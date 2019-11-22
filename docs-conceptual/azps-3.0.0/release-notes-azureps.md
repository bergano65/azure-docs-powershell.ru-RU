---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062145"
---
## <a name="300---november-2019"></a><span data-ttu-id="53aca-103">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="53aca-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="53aca-104">General</span></span>
* <span data-ttu-id="53aca-105">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="53aca-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53aca-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-106">Az.Accounts</span></span>
* <span data-ttu-id="53aca-107">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="53aca-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="53aca-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="53aca-108">Az.Advisor</span></span>
* <span data-ttu-id="53aca-109">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="53aca-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="53aca-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53aca-110">Az.Batch</span></span>
* <span data-ttu-id="53aca-111">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="53aca-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="53aca-112">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="53aca-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="53aca-113">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="53aca-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="53aca-114">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="53aca-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="53aca-115">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="53aca-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="53aca-116">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="53aca-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="53aca-117">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="53aca-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="53aca-118">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="53aca-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="53aca-119">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="53aca-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="53aca-120">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="53aca-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="53aca-121">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="53aca-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="53aca-122">Например, `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="53aca-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="53aca-123">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="53aca-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="53aca-124">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="53aca-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="53aca-125">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="53aca-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="53aca-126">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="53aca-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="53aca-127">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="53aca-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="53aca-128">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="53aca-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="53aca-129">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="53aca-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="53aca-130">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="53aca-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="53aca-131">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="53aca-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="53aca-132">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="53aca-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="53aca-133">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="53aca-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="53aca-134">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="53aca-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="53aca-135">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="53aca-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="53aca-136">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="53aca-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="53aca-137">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="53aca-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="53aca-138">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="53aca-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="53aca-139">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="53aca-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="53aca-140">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="53aca-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="53aca-141">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="53aca-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="53aca-142">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="53aca-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="53aca-143">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="53aca-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="53aca-144">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="53aca-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="53aca-145">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="53aca-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="53aca-146">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="53aca-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53aca-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53aca-147">Az.Cdn</span></span>
* <span data-ttu-id="53aca-148">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="53aca-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="53aca-149">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="53aca-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-150">Az.Compute</span></span>
* <span data-ttu-id="53aca-151">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="53aca-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="53aca-152">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="53aca-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="53aca-153">Добавлен параметр ProximityPlacementGroupId в следующие командлеты: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="53aca-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="53aca-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="53aca-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="53aca-155">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="53aca-156">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="53aca-157">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="53aca-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="53aca-158">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53aca-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="53aca-159">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="53aca-159">Breaking changes</span></span>
    - <span data-ttu-id="53aca-160">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="53aca-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="53aca-161">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="53aca-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-162">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-163">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-165">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="53aca-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="53aca-166">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="53aca-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="53aca-167">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="53aca-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="53aca-168">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="53aca-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="53aca-169">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="53aca-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="53aca-170">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="53aca-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53aca-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53aca-171">Az.FrontDoor</span></span>
* <span data-ttu-id="53aca-172">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="53aca-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="53aca-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53aca-173">Az.HDInsight</span></span>
* <span data-ttu-id="53aca-174">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="53aca-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="53aca-175">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="53aca-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="53aca-176">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="53aca-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="53aca-177">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="53aca-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="53aca-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="53aca-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="53aca-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="53aca-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="53aca-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="53aca-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="53aca-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53aca-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="53aca-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53aca-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="53aca-183">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="53aca-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="53aca-184">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="53aca-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="53aca-185">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="53aca-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="53aca-186">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="53aca-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="53aca-187">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="53aca-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="53aca-188">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="53aca-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="53aca-189">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="53aca-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="53aca-190">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="53aca-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="53aca-191">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="53aca-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="53aca-192">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="53aca-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="53aca-193">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="53aca-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="53aca-194">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="53aca-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="53aca-195">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="53aca-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53aca-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53aca-196">Az.IotHub</span></span>
* <span data-ttu-id="53aca-197">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="53aca-197">Breaking changes:</span></span>
    - <span data-ttu-id="53aca-198">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="53aca-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="53aca-199">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="53aca-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="53aca-200">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="53aca-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="53aca-201">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="53aca-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="53aca-202">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="53aca-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="53aca-203">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="53aca-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="53aca-204">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="53aca-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="53aca-205">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="53aca-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="53aca-206">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="53aca-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="53aca-207">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="53aca-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="53aca-208">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="53aca-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="53aca-209">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="53aca-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-211">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="53aca-212">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="53aca-213">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="53aca-214">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="53aca-215">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="53aca-216">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="53aca-217">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="53aca-218">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="53aca-219">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="53aca-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-220">Az.Resources</span></span>
* <span data-ttu-id="53aca-221">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="53aca-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-222">Az.Network</span></span>
* <span data-ttu-id="53aca-223">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="53aca-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="53aca-224">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="53aca-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="53aca-225">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53aca-226">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53aca-227">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53aca-228">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53aca-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53aca-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="53aca-230">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="53aca-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="53aca-231">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="53aca-231">New cmdlet:</span></span>
        - <span data-ttu-id="53aca-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="53aca-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="53aca-233">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="53aca-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="53aca-234">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53aca-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="53aca-235">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53aca-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="53aca-236">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="53aca-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="53aca-237">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="53aca-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="53aca-238">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="53aca-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="53aca-239">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="53aca-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="53aca-240">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-240">New cmdlets added:</span></span>
        - <span data-ttu-id="53aca-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="53aca-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="53aca-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="53aca-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="53aca-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="53aca-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="53aca-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="53aca-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="53aca-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="53aca-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="53aca-246">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="53aca-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="53aca-247">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="53aca-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="53aca-248">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="53aca-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="53aca-249">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="53aca-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="53aca-250">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="53aca-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="53aca-251">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="53aca-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="53aca-252">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="53aca-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="53aca-253">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-253">New cmdlets added:</span></span>
        - <span data-ttu-id="53aca-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="53aca-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="53aca-255">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="53aca-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="53aca-256">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53aca-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="53aca-257">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53aca-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="53aca-258">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53aca-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="53aca-259">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53aca-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="53aca-260">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53aca-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="53aca-261">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="53aca-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="53aca-262">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-262">New cmdlets added:</span></span>
        - <span data-ttu-id="53aca-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="53aca-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="53aca-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="53aca-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="53aca-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="53aca-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="53aca-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="53aca-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="53aca-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="53aca-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="53aca-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="53aca-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="53aca-269">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="53aca-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="53aca-270">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="53aca-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="53aca-271">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="53aca-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="53aca-272">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="53aca-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="53aca-273">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="53aca-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="53aca-274">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="53aca-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="53aca-275">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="53aca-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="53aca-276">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="53aca-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="53aca-277">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="53aca-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="53aca-278">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="53aca-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="53aca-279">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="53aca-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="53aca-280">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-280">New cmdlets added:</span></span>
        - <span data-ttu-id="53aca-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="53aca-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="53aca-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="53aca-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="53aca-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="53aca-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="53aca-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="53aca-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53aca-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="53aca-286">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="53aca-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-287">Az.Sql</span></span>
* <span data-ttu-id="53aca-288">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="53aca-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="53aca-289">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="53aca-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="53aca-290">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="53aca-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="53aca-291">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="53aca-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="53aca-292">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="53aca-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="53aca-293">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53aca-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="53aca-294">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="53aca-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="53aca-295">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="53aca-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="53aca-296">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="53aca-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-297">Az.Storage</span></span>
* <span data-ttu-id="53aca-298">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="53aca-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="53aca-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="53aca-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="53aca-301">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="53aca-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="53aca-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="53aca-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="53aca-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="53aca-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="53aca-304">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="53aca-305">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="53aca-305">General</span></span>
* <span data-ttu-id="53aca-306">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="53aca-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53aca-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-307">Az.Accounts</span></span>
* <span data-ttu-id="53aca-308">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="53aca-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="53aca-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53aca-309">Az.ApiManagement</span></span>
* <span data-ttu-id="53aca-310">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="53aca-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="53aca-311">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="53aca-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-312">Az.Automation</span></span>
* <span data-ttu-id="53aca-313">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="53aca-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="53aca-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53aca-314">Az.Batch</span></span>
* <span data-ttu-id="53aca-315">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-316">Az.Compute</span></span>
* <span data-ttu-id="53aca-317">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="53aca-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="53aca-318">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="53aca-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="53aca-319">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="53aca-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="53aca-320">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="53aca-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-321">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-322">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="53aca-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="53aca-323">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="53aca-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="53aca-324">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-326">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="53aca-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="53aca-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="53aca-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="53aca-328">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="53aca-329">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="53aca-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="53aca-330">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="53aca-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="53aca-331">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="53aca-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53aca-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53aca-332">Az.IotHub</span></span>
* <span data-ttu-id="53aca-333">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="53aca-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="53aca-334">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="53aca-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="53aca-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53aca-335">Az.Monitor</span></span>
* <span data-ttu-id="53aca-336">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="53aca-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="53aca-337">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="53aca-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="53aca-338">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="53aca-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="53aca-339">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="53aca-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-340">Az.Network</span></span>
* <span data-ttu-id="53aca-341">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="53aca-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="53aca-342">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="53aca-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="53aca-343">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-343">New cmdlets added:</span></span>
        - <span data-ttu-id="53aca-344">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="53aca-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="53aca-345">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="53aca-346">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="53aca-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="53aca-347">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="53aca-348">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="53aca-349">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="53aca-350">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="53aca-351">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="53aca-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="53aca-352">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="53aca-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="53aca-353">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="53aca-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="53aca-354">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="53aca-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="53aca-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="53aca-355">Az.RedisCache</span></span>
* <span data-ttu-id="53aca-356">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="53aca-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-357">Az.Sql</span></span>
* <span data-ttu-id="53aca-358">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="53aca-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-359">Az.Storage</span></span>
* <span data-ttu-id="53aca-360">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="53aca-361">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="53aca-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="53aca-362">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="53aca-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="53aca-363">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="53aca-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="53aca-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="53aca-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="53aca-365">Az.StorageSync</span></span>
* <span data-ttu-id="53aca-366">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="53aca-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-367">Az.Websites</span></span>
* <span data-ttu-id="53aca-368">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="53aca-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="53aca-369">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="53aca-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53aca-370">Az.ApiManagement</span></span>
* <span data-ttu-id="53aca-371">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="53aca-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="53aca-372">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="53aca-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="53aca-373">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53aca-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-374">Az.Automation</span></span>
* <span data-ttu-id="53aca-375">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="53aca-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="53aca-376">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="53aca-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="53aca-377">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="53aca-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-378">Az.Compute</span></span>
* <span data-ttu-id="53aca-379">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="53aca-380">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="53aca-381">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="53aca-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="53aca-382">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="53aca-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="53aca-383">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="53aca-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="53aca-384">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="53aca-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="53aca-385">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="53aca-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="53aca-386">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="53aca-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="53aca-387">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="53aca-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-388">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-389">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="53aca-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="53aca-390">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="53aca-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="53aca-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53aca-391">Az.HDInsight</span></span>
* <span data-ttu-id="53aca-392">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="53aca-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53aca-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53aca-393">Az.IotHub</span></span>
* <span data-ttu-id="53aca-394">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="53aca-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="53aca-395">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="53aca-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="53aca-396">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-396">New cmdlets are:</span></span>
    - <span data-ttu-id="53aca-397">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="53aca-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="53aca-398">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="53aca-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="53aca-399">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="53aca-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="53aca-400">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="53aca-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53aca-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53aca-401">Az.Monitor</span></span>
* <span data-ttu-id="53aca-402">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="53aca-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="53aca-403">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="53aca-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="53aca-404">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="53aca-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="53aca-405">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="53aca-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="53aca-406">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="53aca-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="53aca-407">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="53aca-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="53aca-408">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="53aca-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="53aca-409">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="53aca-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="53aca-410">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="53aca-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="53aca-411">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="53aca-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="53aca-412">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="53aca-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="53aca-413">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="53aca-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="53aca-414">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="53aca-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="53aca-415">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="53aca-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="53aca-416">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="53aca-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="53aca-417">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="53aca-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="53aca-418">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="53aca-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="53aca-419">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="53aca-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="53aca-420">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="53aca-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="53aca-421">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="53aca-421">Overall improved help files</span></span>
* <span data-ttu-id="53aca-422">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="53aca-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-423">Az.Network</span></span>
* <span data-ttu-id="53aca-424">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="53aca-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="53aca-425">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="53aca-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="53aca-426">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="53aca-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="53aca-427">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="53aca-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="53aca-428">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="53aca-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="53aca-429">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="53aca-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="53aca-430">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="53aca-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="53aca-431">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="53aca-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="53aca-432">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="53aca-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="53aca-433">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="53aca-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="53aca-434">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="53aca-435">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="53aca-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="53aca-436">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-436">New cmdlets</span></span>
        - <span data-ttu-id="53aca-437">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="53aca-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="53aca-438">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="53aca-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="53aca-439">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="53aca-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="53aca-440">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="53aca-440">New-VpnSite</span></span>
        - <span data-ttu-id="53aca-441">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="53aca-441">Update-VpnSite</span></span>
        - <span data-ttu-id="53aca-442">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="53aca-442">New-VpnConnection</span></span>
        - <span data-ttu-id="53aca-443">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-443">Update-VpnConnection</span></span>
* <span data-ttu-id="53aca-444">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="53aca-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-446">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="53aca-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="53aca-447">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="53aca-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-448">Az.Resources</span></span>
* <span data-ttu-id="53aca-449">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="53aca-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53aca-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="53aca-451">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="53aca-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="53aca-452">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="53aca-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="53aca-453">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="53aca-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="53aca-454">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="53aca-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="53aca-455">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="53aca-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="53aca-456">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="53aca-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="53aca-457">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="53aca-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="53aca-458">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="53aca-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="53aca-459">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="53aca-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="53aca-460">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="53aca-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="53aca-461">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="53aca-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="53aca-462">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="53aca-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="53aca-463">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="53aca-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="53aca-464">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="53aca-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="53aca-465">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="53aca-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="53aca-466">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="53aca-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="53aca-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="53aca-467">Az.SignalR</span></span>
* <span data-ttu-id="53aca-468">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="53aca-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-469">Az.Sql</span></span>
* <span data-ttu-id="53aca-470">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="53aca-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="53aca-471">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="53aca-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="53aca-472">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="53aca-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="53aca-473">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="53aca-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="53aca-474">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="53aca-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-475">Az.Storage</span></span>
* <span data-ttu-id="53aca-476">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="53aca-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="53aca-477">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="53aca-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="53aca-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="53aca-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="53aca-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="53aca-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="53aca-480">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="53aca-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="53aca-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="53aca-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="53aca-482">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="53aca-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="53aca-483">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="53aca-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="53aca-484">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="53aca-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="53aca-485">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="53aca-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="53aca-486">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="53aca-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-487">Az.Websites</span></span>
* <span data-ttu-id="53aca-488">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="53aca-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="53aca-489">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="53aca-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="53aca-490">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="53aca-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="53aca-491">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="53aca-492">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="53aca-492">General</span></span>
* <span data-ttu-id="53aca-493">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="53aca-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53aca-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-494">Az.Accounts</span></span>
* <span data-ttu-id="53aca-495">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="53aca-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="53aca-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="53aca-496">Az.Aks</span></span>
* <span data-ttu-id="53aca-497">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="53aca-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="53aca-498">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="53aca-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="53aca-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53aca-499">Az.ApiManagement</span></span>
* <span data-ttu-id="53aca-500">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="53aca-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="53aca-501">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="53aca-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="53aca-502">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="53aca-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="53aca-503">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="53aca-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="53aca-504">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="53aca-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="53aca-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53aca-505">Az.Batch</span></span>
* <span data-ttu-id="53aca-506">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="53aca-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53aca-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53aca-507">Az.Cdn</span></span>
* <span data-ttu-id="53aca-508">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="53aca-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-509">Az.Compute</span></span>
* <span data-ttu-id="53aca-510">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="53aca-511">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="53aca-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="53aca-512">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="53aca-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="53aca-513">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="53aca-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="53aca-514">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="53aca-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="53aca-515">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="53aca-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="53aca-516">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="53aca-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="53aca-517">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="53aca-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-518">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-519">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="53aca-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="53aca-520">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="53aca-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="53aca-521">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="53aca-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="53aca-522">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="53aca-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-524">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="53aca-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53aca-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53aca-525">Az.EventHub</span></span>
* <span data-ttu-id="53aca-526">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="53aca-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="53aca-527">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="53aca-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="53aca-528">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="53aca-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="53aca-529">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="53aca-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="53aca-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="53aca-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="53aca-531">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="53aca-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53aca-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53aca-532">Az.Monitor</span></span>
* <span data-ttu-id="53aca-533">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="53aca-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-534">Az.Network</span></span>
* <span data-ttu-id="53aca-535">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="53aca-536">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="53aca-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="53aca-537">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="53aca-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="53aca-538">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="53aca-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="53aca-539">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="53aca-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="53aca-540">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="53aca-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="53aca-541">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="53aca-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53aca-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="53aca-543">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="53aca-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="53aca-544">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="53aca-544">Added example</span></span>
    - <span data-ttu-id="53aca-545">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="53aca-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="53aca-546">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="53aca-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="53aca-547">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="53aca-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-549">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-550">Az.Resources</span></span>
* <span data-ttu-id="53aca-551">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="53aca-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="53aca-552">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="53aca-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="53aca-553">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="53aca-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="53aca-554">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="53aca-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53aca-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53aca-555">Az.ServiceBus</span></span>
* <span data-ttu-id="53aca-556">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="53aca-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="53aca-557">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="53aca-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="53aca-558">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="53aca-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="53aca-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="53aca-560">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="53aca-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="53aca-561">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="53aca-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="53aca-562">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="53aca-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="53aca-563">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="53aca-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="53aca-564">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="53aca-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="53aca-565">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="53aca-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-566">Az.Sql</span></span>
* <span data-ttu-id="53aca-567">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="53aca-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-568">Az.Storage</span></span>
* <span data-ttu-id="53aca-569">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="53aca-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="53aca-570">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="53aca-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="53aca-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="53aca-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="53aca-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53aca-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="53aca-573">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="53aca-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="53aca-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53aca-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-575">Az.Websites</span></span>
* <span data-ttu-id="53aca-576">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="53aca-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="53aca-577">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-578">Az.Accounts</span></span>
* <span data-ttu-id="53aca-579">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="53aca-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="53aca-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="53aca-581">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="53aca-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="53aca-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-582">Az.Automation</span></span>
* <span data-ttu-id="53aca-583">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="53aca-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="53aca-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53aca-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="53aca-585">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="53aca-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-586">Az.Compute</span></span>
* <span data-ttu-id="53aca-587">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="53aca-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="53aca-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="53aca-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="53aca-589">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="53aca-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="53aca-590">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="53aca-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-591">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-592">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="53aca-593">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="53aca-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53aca-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53aca-594">Az.EventHub</span></span>
* <span data-ttu-id="53aca-595">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="53aca-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="53aca-596">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="53aca-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53aca-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53aca-597">Az.KeyVault</span></span>
* <span data-ttu-id="53aca-598">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="53aca-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="53aca-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="53aca-599">Az.LogicApp</span></span>
* <span data-ttu-id="53aca-600">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="53aca-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="53aca-601">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="53aca-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="53aca-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="53aca-602">Az.ManagedServices</span></span>
* <span data-ttu-id="53aca-603">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="53aca-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-604">Az.Network</span></span>
* <span data-ttu-id="53aca-605">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="53aca-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="53aca-606">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-606">New cmdlets</span></span>
        - <span data-ttu-id="53aca-607">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53aca-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="53aca-608">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="53aca-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="53aca-609">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53aca-610">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53aca-611">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53aca-612">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53aca-613">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="53aca-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="53aca-614">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="53aca-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="53aca-615">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="53aca-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="53aca-616">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="53aca-617">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="53aca-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="53aca-618">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="53aca-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="53aca-619">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="53aca-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="53aca-620">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="53aca-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="53aca-621">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-621">Updated cmdlets</span></span>
        - <span data-ttu-id="53aca-622">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="53aca-623">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="53aca-624">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="53aca-625">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="53aca-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="53aca-626">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53aca-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="53aca-627">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="53aca-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="53aca-628">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="53aca-629">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="53aca-630">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="53aca-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="53aca-631">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="53aca-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="53aca-632">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="53aca-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="53aca-633">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="53aca-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53aca-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="53aca-635">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="53aca-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="53aca-636">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="53aca-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-638">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="53aca-639">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="53aca-640">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="53aca-641">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="53aca-642">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="53aca-643">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="53aca-644">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="53aca-645">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="53aca-646">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="53aca-647">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="53aca-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-648">Az.Resources</span></span>
- <span data-ttu-id="53aca-649">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="53aca-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="53aca-650">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="53aca-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53aca-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53aca-651">Az.ServiceBus</span></span>
* <span data-ttu-id="53aca-652">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="53aca-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="53aca-653">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="53aca-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-654">Az.Sql</span></span>
* <span data-ttu-id="53aca-655">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="53aca-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="53aca-656">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="53aca-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="53aca-657">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="53aca-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-658">Az.Storage</span></span>
* <span data-ttu-id="53aca-659">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="53aca-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="53aca-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="53aca-660">Az.StorageSync</span></span>
* <span data-ttu-id="53aca-661">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="53aca-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="53aca-662">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="53aca-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-663">Az.Websites</span></span>
* <span data-ttu-id="53aca-664">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="53aca-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="53aca-665">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="53aca-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="53aca-666">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="53aca-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="53aca-667">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-668">Az.Accounts</span></span>
* <span data-ttu-id="53aca-669">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="53aca-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="53aca-670">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="53aca-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="53aca-671">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="53aca-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="53aca-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="53aca-672">Az.Advisor</span></span>
* <span data-ttu-id="53aca-673">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="53aca-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="53aca-674">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="53aca-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="53aca-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53aca-675">Az.ApiManagement</span></span>
* <span data-ttu-id="53aca-676">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="53aca-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="53aca-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="53aca-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="53aca-678">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="53aca-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="53aca-679">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="53aca-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="53aca-680">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="53aca-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="53aca-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="53aca-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="53aca-682">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="53aca-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-683">Az.Automation</span></span>
* <span data-ttu-id="53aca-684">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="53aca-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-685">Az.Compute</span></span>
* <span data-ttu-id="53aca-686">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="53aca-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-687">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-688">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="53aca-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="53aca-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="53aca-689">Az.EventGrid</span></span>
* <span data-ttu-id="53aca-690">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="53aca-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53aca-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53aca-691">Az.IotHub</span></span>
* <span data-ttu-id="53aca-692">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="53aca-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-693">Az.Network</span></span>
* <span data-ttu-id="53aca-694">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="53aca-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="53aca-695">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="53aca-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53aca-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="53aca-697">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="53aca-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="53aca-698">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="53aca-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53aca-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="53aca-700">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="53aca-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-702">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="53aca-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-703">Az.Resources</span></span>
    - <span data-ttu-id="53aca-704">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="53aca-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="53aca-705">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="53aca-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="53aca-706">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="53aca-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="53aca-707">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="53aca-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53aca-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53aca-708">Az.ServiceBus</span></span>
* <span data-ttu-id="53aca-709">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="53aca-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-710">Az.Sql</span></span>
* <span data-ttu-id="53aca-711">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="53aca-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="53aca-712">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="53aca-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="53aca-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="53aca-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="53aca-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="53aca-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="53aca-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="53aca-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="53aca-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="53aca-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="53aca-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="53aca-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="53aca-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="53aca-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="53aca-719">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="53aca-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-720">Az.Storage</span></span>
* <span data-ttu-id="53aca-721">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="53aca-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="53aca-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="53aca-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="53aca-723">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="53aca-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="53aca-724">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="53aca-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="53aca-725">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="53aca-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="53aca-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="53aca-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="53aca-728">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="53aca-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="53aca-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="53aca-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="53aca-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="53aca-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="53aca-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="53aca-731">Az.StorageSync</span></span>
* <span data-ttu-id="53aca-732">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="53aca-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="53aca-733">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-734">Az.Accounts</span></span>
* <span data-ttu-id="53aca-735">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="53aca-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="53aca-736">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="53aca-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="53aca-737">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="53aca-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="53aca-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="53aca-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="53aca-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="53aca-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-740">Az.Compute</span></span>
* <span data-ttu-id="53aca-741">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="53aca-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="53aca-742">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="53aca-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="53aca-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="53aca-743">Az.Dns</span></span>
* <span data-ttu-id="53aca-744">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="53aca-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="53aca-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="53aca-745">Az.EventGrid</span></span>
* <span data-ttu-id="53aca-746">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="53aca-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="53aca-747">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-747">New cmdlets:</span></span>
    - <span data-ttu-id="53aca-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="53aca-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="53aca-749">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="53aca-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="53aca-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="53aca-751">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="53aca-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="53aca-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="53aca-753">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="53aca-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="53aca-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="53aca-755">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="53aca-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="53aca-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="53aca-757">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="53aca-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="53aca-758">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="53aca-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="53aca-759">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="53aca-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="53aca-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="53aca-761">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="53aca-762">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="53aca-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="53aca-763">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="53aca-764">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="53aca-765">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="53aca-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="53aca-766">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="53aca-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="53aca-767">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="53aca-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="53aca-768">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="53aca-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="53aca-769">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="53aca-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="53aca-770">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="53aca-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="53aca-771">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="53aca-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="53aca-772">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="53aca-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="53aca-773">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="53aca-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="53aca-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="53aca-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="53aca-775">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="53aca-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="53aca-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="53aca-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="53aca-777">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="53aca-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="53aca-778">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="53aca-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53aca-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53aca-779">Az.FrontDoor</span></span>
* <span data-ttu-id="53aca-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="53aca-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="53aca-781">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="53aca-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="53aca-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="53aca-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="53aca-783">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="53aca-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-784">Az.Network</span></span>
* <span data-ttu-id="53aca-785">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="53aca-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="53aca-786">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-786">New cmdlets</span></span>
        - <span data-ttu-id="53aca-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="53aca-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="53aca-788">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="53aca-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="53aca-789">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-789">New cmdlets</span></span> 
        - <span data-ttu-id="53aca-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="53aca-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="53aca-791">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="53aca-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="53aca-792">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-792">New cmdlets</span></span> 
        - <span data-ttu-id="53aca-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53aca-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="53aca-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53aca-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="53aca-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53aca-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="53aca-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="53aca-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53aca-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="53aca-798">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53aca-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="53aca-799">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-799">New cmdlets</span></span>
        - <span data-ttu-id="53aca-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="53aca-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="53aca-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="53aca-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="53aca-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="53aca-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="53aca-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="53aca-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="53aca-804">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="53aca-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="53aca-805">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="53aca-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="53aca-806">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="53aca-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="53aca-807">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="53aca-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="53aca-808">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="53aca-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="53aca-809">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="53aca-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="53aca-810">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53aca-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="53aca-811">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="53aca-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="53aca-812">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53aca-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="53aca-813">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="53aca-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="53aca-814">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="53aca-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="53aca-815">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="53aca-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="53aca-816">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="53aca-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="53aca-817">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="53aca-818">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="53aca-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="53aca-819">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="53aca-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="53aca-820">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="53aca-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="53aca-821">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="53aca-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="53aca-822">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="53aca-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="53aca-823">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="53aca-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="53aca-824">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="53aca-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="53aca-825">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="53aca-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="53aca-826">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="53aca-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53aca-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="53aca-828">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="53aca-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-829">Az.Resources</span></span>
* <span data-ttu-id="53aca-830">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="53aca-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="53aca-831">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="53aca-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="53aca-832">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="53aca-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="53aca-833">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53aca-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53aca-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="53aca-835">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="53aca-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-836">Az.Sql</span></span>
* <span data-ttu-id="53aca-837">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="53aca-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="53aca-838">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="53aca-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="53aca-839">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="53aca-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="53aca-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="53aca-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="53aca-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="53aca-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="53aca-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="53aca-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="53aca-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="53aca-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="53aca-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="53aca-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-845">Az.Storage</span></span>
* <span data-ttu-id="53aca-846">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="53aca-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="53aca-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="53aca-848">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="53aca-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="53aca-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="53aca-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-850">Az.Websites</span></span>
* <span data-ttu-id="53aca-851">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="53aca-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="53aca-852">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="53aca-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="53aca-853">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="53aca-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53aca-854">Az.Cdn</span></span>
* <span data-ttu-id="53aca-855">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="53aca-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-856">Az.Compute</span></span>
* <span data-ttu-id="53aca-857">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="53aca-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="53aca-858">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="53aca-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53aca-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53aca-859">Az.EventHub</span></span>
* <span data-ttu-id="53aca-860">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="53aca-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="53aca-861">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="53aca-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-862">Az.Network</span></span>
* <span data-ttu-id="53aca-863">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="53aca-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="53aca-864">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="53aca-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53aca-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="53aca-866">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="53aca-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-868">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="53aca-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53aca-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53aca-869">Az.ServiceBus</span></span>
* <span data-ttu-id="53aca-870">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="53aca-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53aca-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="53aca-872">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="53aca-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="53aca-873">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="53aca-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-874">Az.Sql</span></span>
* <span data-ttu-id="53aca-875">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="53aca-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="53aca-876">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="53aca-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="53aca-877">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="53aca-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="53aca-878">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="53aca-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-879">Az.Websites</span></span>
* <span data-ttu-id="53aca-880">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="53aca-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="53aca-881">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="53aca-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53aca-882">Az.ApiManagement</span></span>
* <span data-ttu-id="53aca-883">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="53aca-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="53aca-884">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="53aca-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="53aca-885">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="53aca-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="53aca-886">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="53aca-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="53aca-887">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="53aca-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="53aca-888">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="53aca-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="53aca-889">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="53aca-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="53aca-890">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="53aca-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="53aca-891">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53aca-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="53aca-892">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="53aca-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="53aca-893">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="53aca-894">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="53aca-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="53aca-895">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="53aca-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="53aca-896">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="53aca-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="53aca-897">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="53aca-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="53aca-898">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="53aca-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="53aca-899">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="53aca-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="53aca-900">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="53aca-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="53aca-901">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="53aca-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="53aca-902">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="53aca-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="53aca-903">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="53aca-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="53aca-904">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="53aca-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="53aca-905">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="53aca-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="53aca-906">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53aca-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="53aca-907">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="53aca-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="53aca-908">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="53aca-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="53aca-909">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="53aca-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="53aca-910">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53aca-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="53aca-911">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53aca-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="53aca-912">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="53aca-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="53aca-913">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="53aca-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="53aca-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="53aca-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="53aca-915">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="53aca-916">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="53aca-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="53aca-917">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="53aca-918">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="53aca-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="53aca-919">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="53aca-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="53aca-920">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="53aca-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="53aca-921">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="53aca-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="53aca-922">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="53aca-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="53aca-923">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="53aca-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="53aca-924">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="53aca-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="53aca-925">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="53aca-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="53aca-926">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="53aca-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="53aca-927">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="53aca-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="53aca-928">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="53aca-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="53aca-929">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="53aca-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="53aca-930">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="53aca-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="53aca-931">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="53aca-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="53aca-932">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="53aca-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="53aca-933">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="53aca-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="53aca-934">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="53aca-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="53aca-935">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="53aca-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="53aca-936">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="53aca-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="53aca-937">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="53aca-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="53aca-938">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="53aca-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="53aca-939">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="53aca-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="53aca-940">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="53aca-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="53aca-941">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="53aca-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="53aca-942">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="53aca-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="53aca-943">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="53aca-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="53aca-944">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="53aca-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="53aca-945">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="53aca-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="53aca-946">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="53aca-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="53aca-947">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="53aca-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="53aca-948">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="53aca-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="53aca-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="53aca-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="53aca-950">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="53aca-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="53aca-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="53aca-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="53aca-952">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="53aca-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="53aca-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="53aca-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="53aca-954">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="53aca-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="53aca-955">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="53aca-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="53aca-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="53aca-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="53aca-957">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="53aca-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="53aca-958">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="53aca-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="53aca-959">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="53aca-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-960">Az.Automation</span></span>
* <span data-ttu-id="53aca-961">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="53aca-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="53aca-962">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="53aca-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="53aca-963">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="53aca-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="53aca-964">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="53aca-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="53aca-965">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="53aca-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="53aca-966">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="53aca-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="53aca-967">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="53aca-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-968">Az.Compute</span></span>
* <span data-ttu-id="53aca-969">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="53aca-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="53aca-970">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="53aca-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-972">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="53aca-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53aca-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53aca-973">Az.Monitor</span></span>
* <span data-ttu-id="53aca-974">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="53aca-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-975">Az.Network</span></span>
* <span data-ttu-id="53aca-976">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="53aca-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="53aca-977">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="53aca-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="53aca-978">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="53aca-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="53aca-979">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="53aca-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-980">Az.Resources</span></span>
* <span data-ttu-id="53aca-981">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="53aca-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-982">Az.Sql</span></span>
* <span data-ttu-id="53aca-983">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="53aca-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="53aca-984">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-985">Az.Accounts</span></span>
* <span data-ttu-id="53aca-986">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="53aca-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53aca-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53aca-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="53aca-988">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="53aca-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="53aca-989">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="53aca-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-990">Az.Compute</span></span>
* <span data-ttu-id="53aca-991">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="53aca-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="53aca-992">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="53aca-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="53aca-993">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="53aca-994">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="53aca-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="53aca-995">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="53aca-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="53aca-996">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="53aca-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="53aca-997">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="53aca-997">Breaking changes</span></span>
    - <span data-ttu-id="53aca-998">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="53aca-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="53aca-999">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="53aca-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="53aca-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="53aca-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="53aca-1001">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="53aca-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="53aca-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="53aca-1002">Az.Dns</span></span>
* <span data-ttu-id="53aca-1003">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="53aca-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="53aca-1004">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="53aca-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="53aca-1005">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="53aca-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53aca-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53aca-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="53aca-1007">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="53aca-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="53aca-1008">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="53aca-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="53aca-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53aca-1009">Az.HDInsight</span></span>
* <span data-ttu-id="53aca-1010">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="53aca-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="53aca-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53aca-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="53aca-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53aca-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="53aca-1013">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="53aca-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="53aca-1014">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="53aca-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="53aca-1015">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="53aca-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="53aca-1016">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="53aca-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53aca-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53aca-1017">Az.Monitor</span></span>
* <span data-ttu-id="53aca-1018">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="53aca-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="53aca-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="53aca-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="53aca-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="53aca-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="53aca-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="53aca-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="53aca-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="53aca-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="53aca-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="53aca-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="53aca-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="53aca-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="53aca-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53aca-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53aca-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53aca-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53aca-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53aca-1030">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="53aca-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="53aca-1031">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="53aca-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1032">Az.Network</span></span>
* <span data-ttu-id="53aca-1033">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="53aca-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="53aca-1034">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-1034">New cmdlets</span></span>
        - <span data-ttu-id="53aca-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="53aca-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="53aca-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="53aca-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="53aca-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="53aca-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="53aca-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="53aca-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="53aca-1039">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="53aca-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="53aca-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="53aca-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="53aca-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="53aca-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="53aca-1042">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="53aca-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="53aca-1043">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="53aca-1044">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53aca-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="53aca-1046">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="53aca-1047">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="53aca-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="53aca-1048">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="53aca-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-1050">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="53aca-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="53aca-1051">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="53aca-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="53aca-1052">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="53aca-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="53aca-1053">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="53aca-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="53aca-1054">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="53aca-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="53aca-1055">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="53aca-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="53aca-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="53aca-1056">Az.Relay</span></span>
* <span data-ttu-id="53aca-1057">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53aca-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53aca-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="53aca-1059">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="53aca-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-1060">Az.Storage</span></span>
* <span data-ttu-id="53aca-1061">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="53aca-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="53aca-1062">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="53aca-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="53aca-1063">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="53aca-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="53aca-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="53aca-1065">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="53aca-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="53aca-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="53aca-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="53aca-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1069">Az.Websites</span></span>
* <span data-ttu-id="53aca-1070">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="53aca-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="53aca-1071">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="53aca-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="53aca-1072">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53aca-1073">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="53aca-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="53aca-1074">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="53aca-1075">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="53aca-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="53aca-1076">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="53aca-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="53aca-1077">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="53aca-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="53aca-1078">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="53aca-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="53aca-1079">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="53aca-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="53aca-1080">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="53aca-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53aca-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-1081">Az.Accounts</span></span>
* <span data-ttu-id="53aca-1082">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="53aca-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="53aca-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53aca-1083">Az.Batch</span></span>
* <span data-ttu-id="53aca-1084">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53aca-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53aca-1085">Az.Cdn</span></span>
* <span data-ttu-id="53aca-1086">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53aca-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="53aca-1088">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1089">Az.Compute</span></span>
* <span data-ttu-id="53aca-1090">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="53aca-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="53aca-1091">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53aca-1092">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="53aca-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-1093">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-1094">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="53aca-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-1096">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="53aca-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="53aca-1097">Az.EventGrid</span></span>
* <span data-ttu-id="53aca-1098">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="53aca-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53aca-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53aca-1099">Az.EventHub</span></span>
* <span data-ttu-id="53aca-1100">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="53aca-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="53aca-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53aca-1101">Az.HDInsight</span></span>
* <span data-ttu-id="53aca-1102">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53aca-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53aca-1103">Az.IotHub</span></span>
* <span data-ttu-id="53aca-1104">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53aca-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53aca-1105">Az.KeyVault</span></span>
* <span data-ttu-id="53aca-1106">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53aca-1107">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="53aca-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="53aca-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="53aca-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="53aca-1109">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="53aca-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="53aca-1110">Az.Media</span></span>
* <span data-ttu-id="53aca-1111">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53aca-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53aca-1112">Az.Monitor</span></span>
  * <span data-ttu-id="53aca-1113">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="53aca-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="53aca-1114">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="53aca-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="53aca-1115">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="53aca-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="53aca-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="53aca-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="53aca-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="53aca-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="53aca-1118">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="53aca-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="53aca-1119">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1120">Az.Network</span></span>
* <span data-ttu-id="53aca-1121">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53aca-1122">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="53aca-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="53aca-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="53aca-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="53aca-1124">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53aca-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="53aca-1126">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="53aca-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="53aca-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="53aca-1128">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-1130">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53aca-1131">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="53aca-1132">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="53aca-1133">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="53aca-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="53aca-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="53aca-1134">Az.RedisCache</span></span>
* <span data-ttu-id="53aca-1135">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1136">Az.Resources</span></span>
* <span data-ttu-id="53aca-1137">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="53aca-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1138">Az.Sql</span></span>
* <span data-ttu-id="53aca-1139">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="53aca-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="53aca-1140">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53aca-1141">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="53aca-1142">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="53aca-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="53aca-1143">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="53aca-1144">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="53aca-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="53aca-1145">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="53aca-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1146">Az.Websites</span></span>
* <span data-ttu-id="53aca-1147">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="53aca-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="53aca-1148">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="53aca-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53aca-1149">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="53aca-1150">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="53aca-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="53aca-1151">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53aca-1152">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="53aca-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="53aca-1153">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="53aca-1154">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="53aca-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="53aca-1155">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="53aca-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="53aca-1156">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="53aca-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="53aca-1157">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="53aca-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="53aca-1158">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="53aca-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="53aca-1159">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="53aca-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53aca-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-1160">Az.Accounts</span></span>
* <span data-ttu-id="53aca-1161">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="53aca-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="53aca-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="53aca-1163">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="53aca-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="53aca-1164">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="53aca-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-1165">Az.Automation</span></span>
* <span data-ttu-id="53aca-1166">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="53aca-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="53aca-1167">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="53aca-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="53aca-1168">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1169">Az.Compute</span></span>
* <span data-ttu-id="53aca-1170">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="53aca-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="53aca-1171">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="53aca-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="53aca-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="53aca-1173">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="53aca-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-1174">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-1175">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="53aca-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="53aca-1176">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53aca-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1177">Az.Resources</span></span>
* <span data-ttu-id="53aca-1178">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="53aca-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="53aca-1179">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="53aca-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="53aca-1180">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="53aca-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="53aca-1181">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="53aca-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="53aca-1182">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="53aca-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="53aca-1183">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="53aca-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1184">Az.Sql</span></span>
* <span data-ttu-id="53aca-1185">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="53aca-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-1186">Az.Storage</span></span>
* <span data-ttu-id="53aca-1187">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="53aca-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="53aca-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="53aca-1189">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="53aca-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="53aca-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="53aca-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="53aca-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="53aca-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="53aca-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="53aca-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="53aca-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="53aca-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="53aca-1194">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="53aca-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="53aca-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="53aca-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="53aca-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="53aca-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="53aca-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="53aca-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="53aca-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="53aca-1199">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53aca-1200">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="53aca-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="53aca-1201">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="53aca-1202">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="53aca-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="53aca-1203">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="53aca-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="53aca-1204">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="53aca-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="53aca-1205">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="53aca-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="53aca-1206">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="53aca-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="53aca-1207">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="53aca-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-1208">Az.Automation</span></span>
* <span data-ttu-id="53aca-1209">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="53aca-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="53aca-1210">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="53aca-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="53aca-1211">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="53aca-1211">Pre-Post script</span></span>
    * <span data-ttu-id="53aca-1212">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1213">Az.Compute</span></span>
* <span data-ttu-id="53aca-1214">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="53aca-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="53aca-1215">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53aca-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53aca-1216">Az.KeyVault</span></span>
* <span data-ttu-id="53aca-1217">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="53aca-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1218">Az.Network</span></span>
* <span data-ttu-id="53aca-1219">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="53aca-1220">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="53aca-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-1222">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="53aca-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="53aca-1223">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="53aca-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1224">Az.Resources</span></span>
* <span data-ttu-id="53aca-1225">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="53aca-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="53aca-1226">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="53aca-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1227">Az.Sql</span></span>
* <span data-ttu-id="53aca-1228">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="53aca-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-1229">Az.Storage</span></span>
* <span data-ttu-id="53aca-1230">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="53aca-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="53aca-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="53aca-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="53aca-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="53aca-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="53aca-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="53aca-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="53aca-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="53aca-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="53aca-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="53aca-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="53aca-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1237">Az.Websites</span></span>
* <span data-ttu-id="53aca-1238">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="53aca-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="53aca-1239">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-1240">Az.Accounts</span></span>
* <span data-ttu-id="53aca-1241">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="53aca-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="53aca-1242">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="53aca-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-1243">Az.Automation</span></span>
* <span data-ttu-id="53aca-1244">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="53aca-1245">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="53aca-1246">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="53aca-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53aca-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53aca-1247">Az.Cdn</span></span>
* <span data-ttu-id="53aca-1248">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="53aca-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1249">Az.Compute</span></span>
* <span data-ttu-id="53aca-1250">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="53aca-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-1251">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-1252">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="53aca-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="53aca-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="53aca-1253">Az.LogicApp</span></span>
* <span data-ttu-id="53aca-1254">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="53aca-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1255">Az.Network</span></span>
* <span data-ttu-id="53aca-1256">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="53aca-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-1258">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="53aca-1259">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="53aca-1259">SDK Update</span></span>
* <span data-ttu-id="53aca-1260">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="53aca-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="53aca-1261">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="53aca-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1262">Az.Resources</span></span>
* <span data-ttu-id="53aca-1263">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="53aca-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="53aca-1264">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="53aca-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="53aca-1265">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="53aca-1266">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="53aca-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="53aca-1267">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="53aca-1268">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="53aca-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1269">Az.Sql</span></span>
* <span data-ttu-id="53aca-1270">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="53aca-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="53aca-1271">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="53aca-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-1272">Az.Storage</span></span>
* <span data-ttu-id="53aca-1273">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="53aca-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="53aca-1274">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="53aca-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="53aca-1276">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="53aca-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-1277">Az.Automation</span></span>
* <span data-ttu-id="53aca-1278">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53aca-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="53aca-1279">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53aca-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="53aca-1280">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53aca-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53aca-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="53aca-1282">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="53aca-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1283">Az.Compute</span></span>
* <span data-ttu-id="53aca-1284">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="53aca-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="53aca-1285">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="53aca-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="53aca-1286">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="53aca-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="53aca-1287">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="53aca-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-1289">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="53aca-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53aca-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53aca-1290">Az.EventHub</span></span>
* <span data-ttu-id="53aca-1291">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="53aca-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="53aca-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53aca-1292">Az.KeyVault</span></span>
* <span data-ttu-id="53aca-1293">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="53aca-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="53aca-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="53aca-1294">Az.LogicApp</span></span>
* <span data-ttu-id="53aca-1295">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="53aca-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="53aca-1296">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="53aca-1297">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="53aca-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="53aca-1298">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="53aca-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="53aca-1299">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="53aca-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="53aca-1300">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="53aca-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="53aca-1301">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="53aca-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="53aca-1302">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="53aca-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="53aca-1303">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="53aca-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="53aca-1304">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="53aca-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="53aca-1305">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="53aca-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="53aca-1306">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53aca-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="53aca-1307">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53aca-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53aca-1308">Az.Monitor</span></span>
* <span data-ttu-id="53aca-1309">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="53aca-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1310">Az.Network</span></span>
* <span data-ttu-id="53aca-1311">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="53aca-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53aca-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="53aca-1313">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="53aca-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="53aca-1314">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="53aca-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="53aca-1315">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="53aca-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="53aca-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1316">Az.Resources</span></span>
* <span data-ttu-id="53aca-1317">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="53aca-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="53aca-1318">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="53aca-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="53aca-1319">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="53aca-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="53aca-1320">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="53aca-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1321">Az.Sql</span></span>
* <span data-ttu-id="53aca-1322">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="53aca-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="53aca-1323">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="53aca-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1324">Az.Websites</span></span>
* <span data-ttu-id="53aca-1325">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="53aca-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="53aca-1326">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-1327">Az.Accounts</span></span>
* <span data-ttu-id="53aca-1328">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="53aca-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="53aca-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="53aca-1330">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="53aca-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1331">Az.Compute</span></span>
* <span data-ttu-id="53aca-1332">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="53aca-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="53aca-1333">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="53aca-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="53aca-1334">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="53aca-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="53aca-1336">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="53aca-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1337">Az.Resources</span></span>
* <span data-ttu-id="53aca-1338">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="53aca-1339">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="53aca-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="53aca-1340">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="53aca-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="53aca-1341">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="53aca-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1342">Az.Sql</span></span>
* <span data-ttu-id="53aca-1343">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="53aca-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="53aca-1344">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="53aca-1345">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="53aca-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="53aca-1346">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-1347">Az.Accounts</span></span>
* <span data-ttu-id="53aca-1348">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="53aca-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="53aca-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="53aca-1350">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="53aca-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="53aca-1352">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="53aca-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="53aca-1353">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-1354">Az.Accounts</span></span>
* <span data-ttu-id="53aca-1355">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="53aca-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="53aca-1356">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="53aca-1357">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="53aca-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="53aca-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="53aca-1358">Az.Aks</span></span>
* <span data-ttu-id="53aca-1359">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53aca-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-1360">Az.Automation</span></span>
* <span data-ttu-id="53aca-1361">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="53aca-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="53aca-1362">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53aca-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53aca-1363">Az.Cdn</span></span>
* <span data-ttu-id="53aca-1364">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1365">Az.Compute</span></span>
* <span data-ttu-id="53aca-1366">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="53aca-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="53aca-1367">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="53aca-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="53aca-1368">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="53aca-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="53aca-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="53aca-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="53aca-1370">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53aca-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53aca-1371">Az.DataFactory</span></span>
* <span data-ttu-id="53aca-1372">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-1374">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="53aca-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="53aca-1375">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="53aca-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="53aca-1376">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53aca-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53aca-1377">Az.IotHub</span></span>
* <span data-ttu-id="53aca-1378">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53aca-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53aca-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53aca-1379">Az.KeyVault</span></span>
* <span data-ttu-id="53aca-1380">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1381">Az.Network</span></span>
* <span data-ttu-id="53aca-1382">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1383">Az.Resources</span></span>
* <span data-ttu-id="53aca-1384">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="53aca-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="53aca-1385">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="53aca-1386">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="53aca-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="53aca-1387">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="53aca-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="53aca-1388">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="53aca-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="53aca-1389">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="53aca-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="53aca-1390">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="53aca-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53aca-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="53aca-1392">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="53aca-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="53aca-1393">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="53aca-1393">Fix some error messages.</span></span>
* <span data-ttu-id="53aca-1394">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="53aca-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="53aca-1395">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="53aca-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="53aca-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="53aca-1396">Az.SignalR</span></span>
* <span data-ttu-id="53aca-1397">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1398">Az.Sql</span></span>
* <span data-ttu-id="53aca-1399">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="53aca-1400">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="53aca-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="53aca-1401">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="53aca-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="53aca-1402">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="53aca-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-1403">Az.Storage</span></span>
* <span data-ttu-id="53aca-1404">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="53aca-1405">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="53aca-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="53aca-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="53aca-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="53aca-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="53aca-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="53aca-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="53aca-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="53aca-1409">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1410">Az.Websites</span></span>
* <span data-ttu-id="53aca-1411">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="53aca-1412">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="53aca-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="53aca-1413">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="53aca-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="53aca-1414">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53aca-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-1415">Az.Accounts</span></span>
* <span data-ttu-id="53aca-1416">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="53aca-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1417">Az.Compute</span></span>
* <span data-ttu-id="53aca-1418">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="53aca-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="53aca-1419">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="53aca-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="53aca-1420">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="53aca-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-1422">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="53aca-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="53aca-1423">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="53aca-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="53aca-1424">Az.EventGrid</span></span>
* <span data-ttu-id="53aca-1425">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="53aca-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="53aca-1426">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="53aca-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="53aca-1427">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="53aca-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="53aca-1428">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="53aca-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="53aca-1429">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="53aca-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="53aca-1430">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="53aca-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="53aca-1431">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="53aca-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="53aca-1432">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="53aca-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="53aca-1433">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="53aca-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="53aca-1434">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="53aca-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="53aca-1435">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="53aca-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="53aca-1436">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="53aca-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53aca-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53aca-1437">Az.IotHub</span></span>
* <span data-ttu-id="53aca-1438">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="53aca-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="53aca-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="53aca-1439">Az.LogicApp</span></span>
* <span data-ttu-id="53aca-1440">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="53aca-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1441">Az.Resources</span></span>
* <span data-ttu-id="53aca-1442">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="53aca-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="53aca-1443">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="53aca-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="53aca-1444">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="53aca-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="53aca-1445">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="53aca-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="53aca-1446">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="53aca-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="53aca-1447">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="53aca-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="53aca-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="53aca-1448">Az.SignalR</span></span>
* <span data-ttu-id="53aca-1449">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="53aca-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1450">Az.Sql</span></span>
* <span data-ttu-id="53aca-1451">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="53aca-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53aca-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-1452">Az.Storage</span></span>
* <span data-ttu-id="53aca-1453">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="53aca-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="53aca-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="53aca-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="53aca-1455">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="53aca-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="53aca-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="53aca-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1457">Az.Websites</span></span>
* <span data-ttu-id="53aca-1458">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="53aca-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="53aca-1459">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="53aca-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="53aca-1460">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="53aca-1461">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="53aca-1461">General</span></span>

- <span data-ttu-id="53aca-1462">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="53aca-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="53aca-1463">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="53aca-1463">Online help for each module</span></span>
- <span data-ttu-id="53aca-1464">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="53aca-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="53aca-1465">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="53aca-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53aca-1466">Az.Accounts</span></span>
- <span data-ttu-id="53aca-1467">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="53aca-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="53aca-1468">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="53aca-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="53aca-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53aca-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="53aca-1470">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="53aca-1470">Fixes for #7002</span></span>
- <span data-ttu-id="53aca-1471">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="53aca-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53aca-1472">Az.Batch</span></span>
- <span data-ttu-id="53aca-1473">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="53aca-1474">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="53aca-1475">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="53aca-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="53aca-1476">Az.Billing</span></span>
- <span data-ttu-id="53aca-1477">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="53aca-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="53aca-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="53aca-1479">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="53aca-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="53aca-1480">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="53aca-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="53aca-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="53aca-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="53aca-1482">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="53aca-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="53aca-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="53aca-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="53aca-1484">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="53aca-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="53aca-1486">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="53aca-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53aca-1487">Az.Monitor</span></span>
- <span data-ttu-id="53aca-1488">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="53aca-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53aca-1489">Az.KeyVault</span></span>
- <span data-ttu-id="53aca-1490">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="53aca-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="53aca-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="53aca-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="53aca-1492">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="53aca-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="53aca-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="53aca-1493">Az.Media</span></span>
- <span data-ttu-id="53aca-1494">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="53aca-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="53aca-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1495">Az.Network</span></span>
<span data-ttu-id="53aca-1496">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="53aca-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="53aca-1497">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="53aca-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53aca-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53aca-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53aca-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53aca-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53aca-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53aca-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53aca-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53aca-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53aca-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53aca-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="53aca-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="53aca-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="53aca-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="53aca-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="53aca-1506">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53aca-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="53aca-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53aca-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="53aca-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="53aca-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="53aca-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="53aca-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="53aca-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="53aca-1512">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="53aca-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="53aca-1513">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="53aca-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="53aca-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53aca-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="53aca-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53aca-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="53aca-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53aca-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="53aca-1517">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="53aca-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="53aca-1518">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="53aca-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="53aca-1520">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="53aca-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="53aca-1521">Az.Profile</span></span>
- <span data-ttu-id="53aca-1522">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="53aca-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="53aca-1524">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="53aca-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1525">Az.Resources</span></span>
- <span data-ttu-id="53aca-1526">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="53aca-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="53aca-1528">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="53aca-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="53aca-1529">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="53aca-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="53aca-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="53aca-1531">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="53aca-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="53aca-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1532">Az.Sql</span></span>
- <span data-ttu-id="53aca-1533">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="53aca-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="53aca-1534">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="53aca-1535">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="53aca-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-1536">Az.Storage</span></span>
- <span data-ttu-id="53aca-1537">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="53aca-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1538">Az.Websites</span></span>
- <span data-ttu-id="53aca-1539">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="53aca-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="53aca-1540">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="53aca-1541">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="53aca-1541">General</span></span>

* <span data-ttu-id="53aca-1542">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="53aca-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="53aca-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1543">Az.Compute</span></span>

* <span data-ttu-id="53aca-1544">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="53aca-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="53aca-1546">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="53aca-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="53aca-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53aca-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="53aca-1548">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="53aca-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="53aca-1549">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="53aca-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="53aca-1550">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="53aca-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="53aca-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="53aca-1552">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="53aca-1553">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="53aca-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="53aca-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1554">Az.Resources</span></span>

* <span data-ttu-id="53aca-1555">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="53aca-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="53aca-1556">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="53aca-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1557">Az.Sql</span></span>

* <span data-ttu-id="53aca-1558">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="53aca-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="53aca-1559">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="53aca-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="53aca-1560">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="53aca-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="53aca-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53aca-1561">Az.Storage</span></span>

* <span data-ttu-id="53aca-1562">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="53aca-1563">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="53aca-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="53aca-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="53aca-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="53aca-1565">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="53aca-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="53aca-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="53aca-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="53aca-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="53aca-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="53aca-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1568">Az.Websites</span></span>

* <span data-ttu-id="53aca-1569">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53aca-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="53aca-1570">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="53aca-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="53aca-1571">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="53aca-1572">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="53aca-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53aca-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="53aca-1574">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="53aca-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53aca-1575">Az.Automation</span></span>
* <span data-ttu-id="53aca-1576">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="53aca-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="53aca-1577">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="53aca-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="53aca-1578">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="53aca-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="53aca-1579">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="53aca-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="53aca-1580">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="53aca-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="53aca-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1581">Az.Compute</span></span>
* <span data-ttu-id="53aca-1582">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="53aca-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="53aca-1583">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="53aca-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="53aca-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="53aca-1585">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="53aca-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="53aca-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="53aca-1587">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="53aca-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="53aca-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1588">Az.Network</span></span>
* <span data-ttu-id="53aca-1589">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="53aca-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="53aca-1590">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="53aca-1591">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="53aca-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="53aca-1592">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="53aca-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="53aca-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="53aca-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="53aca-1594">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="53aca-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="53aca-1595">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="53aca-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="53aca-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="53aca-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="53aca-1597">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="53aca-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="53aca-1598">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="53aca-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="53aca-1599">Az.Relay</span></span>
* <span data-ttu-id="53aca-1600">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="53aca-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="53aca-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1601">Az.Resources</span></span>
* <span data-ttu-id="53aca-1602">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="53aca-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="53aca-1603">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="53aca-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="53aca-1604">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="53aca-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="53aca-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="53aca-1606">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="53aca-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="53aca-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1607">Az.Sql</span></span>
* <span data-ttu-id="53aca-1608">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="53aca-1609">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="53aca-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="53aca-1610">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="53aca-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="53aca-1611">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="53aca-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="53aca-1612">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="53aca-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="53aca-1613">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="53aca-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="53aca-1614">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="53aca-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="53aca-1615">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="53aca-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="53aca-1616">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="53aca-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="53aca-1617">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="53aca-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="53aca-1618">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="53aca-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="53aca-1619">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="53aca-1620">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="53aca-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="53aca-1621">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="53aca-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="53aca-1622">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="53aca-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="53aca-1623">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="53aca-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="53aca-1624">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="53aca-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="53aca-1625">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="53aca-1626">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="53aca-1626">General</span></span>
* <span data-ttu-id="53aca-1627">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="53aca-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="53aca-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="53aca-1628">Az.Profile</span></span>
* <span data-ttu-id="53aca-1629">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="53aca-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="53aca-1630">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="53aca-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="53aca-1631">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="53aca-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="53aca-1632">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="53aca-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="53aca-1633">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="53aca-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="53aca-1634">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="53aca-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="53aca-1635">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="53aca-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="53aca-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="53aca-1637">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="53aca-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1638">Az.Compute</span></span>
* <span data-ttu-id="53aca-1639">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="53aca-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="53aca-1640">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="53aca-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="53aca-1641">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="53aca-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-1643">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="53aca-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="53aca-1644">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="53aca-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="53aca-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="53aca-1645">Az.Insights</span></span>
* <span data-ttu-id="53aca-1646">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="53aca-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="53aca-1647">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="53aca-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="53aca-1648">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="53aca-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="53aca-1649">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="53aca-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1650">Az.Network</span></span>
* <span data-ttu-id="53aca-1651">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="53aca-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="53aca-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="53aca-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="53aca-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="53aca-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="53aca-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="53aca-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="53aca-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="53aca-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="53aca-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="53aca-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="53aca-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="53aca-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53aca-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53aca-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="53aca-1659">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="53aca-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1660">Az.Resources</span></span>
* <span data-ttu-id="53aca-1661">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="53aca-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="53aca-1662">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="53aca-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53aca-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53aca-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="53aca-1664">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="53aca-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53aca-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53aca-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="53aca-1666">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="53aca-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="53aca-1667">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="53aca-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="53aca-1668">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="53aca-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="53aca-1669">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="53aca-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="53aca-1670">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="53aca-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="53aca-1671">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="53aca-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="53aca-1672">Az.Profile</span></span>
* <span data-ttu-id="53aca-1673">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="53aca-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="53aca-1674">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="53aca-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1675">Az.Compute</span></span>
* <span data-ttu-id="53aca-1676">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="53aca-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="53aca-1677">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="53aca-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53aca-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53aca-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="53aca-1679">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="53aca-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="53aca-1680">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53aca-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="53aca-1681">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53aca-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="53aca-1682">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53aca-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="53aca-1683">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53aca-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1684">Az.Network</span></span>
* <span data-ttu-id="53aca-1685">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="53aca-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="53aca-1686">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="53aca-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1687">Az.Resources</span></span>
* <span data-ttu-id="53aca-1688">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="53aca-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="53aca-1689">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="53aca-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="53aca-1690">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="53aca-1691">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="53aca-1691">Azure.Storage</span></span>
* <span data-ttu-id="53aca-1692">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="53aca-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="53aca-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53aca-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="53aca-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="53aca-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="53aca-1695">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="53aca-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="53aca-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="53aca-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="53aca-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53aca-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="53aca-1698">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="53aca-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53aca-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53aca-1699">Az.Compute</span></span>
* <span data-ttu-id="53aca-1700">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="53aca-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="53aca-1701">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="53aca-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="53aca-1702">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="53aca-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="53aca-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="53aca-1704">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="53aca-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53aca-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53aca-1705">Az.Network</span></span>
* <span data-ttu-id="53aca-1706">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="53aca-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="53aca-1707">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="53aca-1707">new cmdlets added</span></span>
    - <span data-ttu-id="53aca-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53aca-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="53aca-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53aca-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="53aca-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53aca-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="53aca-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53aca-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="53aca-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="53aca-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="53aca-1714">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="53aca-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="53aca-1715">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="53aca-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="53aca-1716">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="53aca-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="53aca-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="53aca-1717">Az.RedisCache</span></span>
* <span data-ttu-id="53aca-1718">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="53aca-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="53aca-1719">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="53aca-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="53aca-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53aca-1720">Az.Resources</span></span>
* <span data-ttu-id="53aca-1721">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="53aca-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="53aca-1722">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="53aca-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="53aca-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53aca-1723">Az.Sql</span></span>
* <span data-ttu-id="53aca-1724">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="53aca-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53aca-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53aca-1725">Az.Websites</span></span>
* <span data-ttu-id="53aca-1726">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="53aca-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="53aca-1727">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="53aca-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="53aca-1728">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="53aca-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="53aca-1729">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="53aca-1729">Initial Release</span></span>
