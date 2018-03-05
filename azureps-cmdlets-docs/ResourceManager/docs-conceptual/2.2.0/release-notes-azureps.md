---
title: "Журнал изменений Azure PowerShell | Документация Майкрософт"
description: "Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: 
ms.date: 05/18/2017
ms.openlocfilehash: 143d92384fd270711378f6741ba59e88c12833d1
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <a name="release-notes"></a><span data-ttu-id="94ce6-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="94ce6-103">Release notes</span></span>

<span data-ttu-id="94ce6-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="94ce6-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="94ce6-105">Версия 2.2.0</span><span class="sxs-lookup"><span data-stu-id="94ce6-105">Version 2.2.0</span></span>
* <span data-ttu-id="94ce6-106">Среда выполнения приложений</span><span class="sxs-lookup"><span data-stu-id="94ce6-106">Compute</span></span>
  - <span data-ttu-id="94ce6-107">Добавлена поддержка для запроса состояния шифрования из расширения AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="94ce6-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="94ce6-108">Фабрика данных</span><span class="sxs-lookup"><span data-stu-id="94ce6-108">DataFactory</span></span>
  - <span data-ttu-id="94ce6-109">Добавлен новый командлет для перечисления окон действий:</span><span class="sxs-lookup"><span data-stu-id="94ce6-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="94ce6-110">Get-AzureRmDataFactoryActivityWindow.</span><span class="sxs-lookup"><span data-stu-id="94ce6-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="94ce6-111">Data Lake</span><span class="sxs-lookup"><span data-stu-id="94ce6-111">DataLake</span></span>
  - <span data-ttu-id="94ce6-112">В следующих командлетах параметр `Host` изменен на `DatabaseHost`, а в `Host` добавлен псевдоним:</span><span class="sxs-lookup"><span data-stu-id="94ce6-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="94ce6-113">New-AzureRmDataLakeAnalyticsCatalogSecret;</span><span class="sxs-lookup"><span data-stu-id="94ce6-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="94ce6-114">Set-AzureRmDataLakeAnalyticsCatalogSecret.</span><span class="sxs-lookup"><span data-stu-id="94ce6-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="94ce6-115">Добавлена поддержка для удаления списка ACL и списка ACL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94ce6-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="94ce6-116">Добавлена поддержка для получения и настройки разрешений без имени для файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="94ce6-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="94ce6-117">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="94ce6-117">KeyVault</span></span>
  - <span data-ttu-id="94ce6-118">Добавлена поддержка следующих сертификатов:</span><span class="sxs-lookup"><span data-stu-id="94ce6-118">Add support for certificates</span></span>
    + <span data-ttu-id="94ce6-119">Add-AzureKeyVaultCertificate;</span><span class="sxs-lookup"><span data-stu-id="94ce6-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="94ce6-120">Add-AzureKeyVaultCertificateContact;</span><span class="sxs-lookup"><span data-stu-id="94ce6-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="94ce6-121">Get-AzureKeyVaultCertificate;</span><span class="sxs-lookup"><span data-stu-id="94ce6-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="94ce6-122">Get-AzureKeyVaultCertificateContact;</span><span class="sxs-lookup"><span data-stu-id="94ce6-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="94ce6-123">Get-AzureKeyVaultCertificateIssuer;</span><span class="sxs-lookup"><span data-stu-id="94ce6-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="94ce6-124">Get-AzureKeyVaultCertificateOperation;</span><span class="sxs-lookup"><span data-stu-id="94ce6-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="94ce6-125">Get-AzureKeyVaultCertificatePolicy;</span><span class="sxs-lookup"><span data-stu-id="94ce6-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="94ce6-126">Import-AzureKeyVaultCertificate;</span><span class="sxs-lookup"><span data-stu-id="94ce6-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="94ce6-127">New-AzureKeyVaultCertificateAdministratorDetails;</span><span class="sxs-lookup"><span data-stu-id="94ce6-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="94ce6-128">New-AzureKeyVaultCertificateOrganizationDetails;</span><span class="sxs-lookup"><span data-stu-id="94ce6-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="94ce6-129">New-AzureKeyVaultCertificatePolicy;</span><span class="sxs-lookup"><span data-stu-id="94ce6-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="94ce6-130">Remove-AzureKeyVaultCertificate;</span><span class="sxs-lookup"><span data-stu-id="94ce6-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="94ce6-131">Remove-AzureKeyVaultCertificateContact;</span><span class="sxs-lookup"><span data-stu-id="94ce6-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="94ce6-132">Remove-AzureKeyVaultCertificateIssuer;</span><span class="sxs-lookup"><span data-stu-id="94ce6-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="94ce6-133">Remove-AzureKeyVaultCertificateOperation;</span><span class="sxs-lookup"><span data-stu-id="94ce6-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="94ce6-134">Set-AzureKeyVaultCertificateAttribute;</span><span class="sxs-lookup"><span data-stu-id="94ce6-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="94ce6-135">Set-AzureKeyVaultCertificateIssuer;</span><span class="sxs-lookup"><span data-stu-id="94ce6-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="94ce6-136">Set-AzureKeyVaultCertificatePolicy;</span><span class="sxs-lookup"><span data-stu-id="94ce6-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="94ce6-137">Stop-AzureKeyVaultCertificateOperation.</span><span class="sxs-lookup"><span data-stu-id="94ce6-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="94ce6-138">Сеть</span><span class="sxs-lookup"><span data-stu-id="94ce6-138">Network</span></span>

  - <span data-ttu-id="94ce6-139">Для сетевого интерфейса добавлен новый параметр переключателя, чтобы включить или отключить ускорение работы в сети — +New-AzureRmNetworkInterface -EnableAcceleratedNetworking.</span><span class="sxs-lookup"><span data-stu-id="94ce6-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="94ce6-140">Добавлены командлеты PowerShell для включения функций шлюза в режиме "активный-активный":</span><span class="sxs-lookup"><span data-stu-id="94ce6-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="94ce6-141">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="94ce6-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="94ce6-142">Remove-AzureRmVirtualNetworkGatewayIpConfig.</span><span class="sxs-lookup"><span data-stu-id="94ce6-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="94ce6-143">Добавлен новый командлет:</span><span class="sxs-lookup"><span data-stu-id="94ce6-143">Added new cmdlet</span></span>
    + <span data-ttu-id="94ce6-144">Test-AzureRmPrivateIpAddressAvailability.</span><span class="sxs-lookup"><span data-stu-id="94ce6-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="94ce6-145">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="94ce6-145">Resources</span></span>
  - <span data-ttu-id="94ce6-146">Добавлена поддержка зон в командлетах поставщика и ресурсов:</span><span class="sxs-lookup"><span data-stu-id="94ce6-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="94ce6-147">Get-AzureRmProvider;</span><span class="sxs-lookup"><span data-stu-id="94ce6-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="94ce6-148">New-AzureRmResource;</span><span class="sxs-lookup"><span data-stu-id="94ce6-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="94ce6-149">Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="94ce6-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="94ce6-150">SQL</span><span class="sxs-lookup"><span data-stu-id="94ce6-150">Sql</span></span>
  - <span data-ttu-id="94ce6-151">Добавлены новые командлеты для управления политикой обнаружения угроз SQL Azure на уровне сервера:</span><span class="sxs-lookup"><span data-stu-id="94ce6-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="94ce6-152">Get-AzureRmSqlServerThreatDetectionPolicy;</span><span class="sxs-lookup"><span data-stu-id="94ce6-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="94ce6-153">Remove-AzureRmSqlServerThreatDetectionPolicy;</span><span class="sxs-lookup"><span data-stu-id="94ce6-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="94ce6-154">Set-AzureRmSqlServerThreatDetectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="94ce6-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="94ce6-155">Добавлены новые командлеты для поддержки включения или отключения GeoBackupPolicy для Sql Azure DataWarehouses:</span><span class="sxs-lookup"><span data-stu-id="94ce6-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="94ce6-156">Get-AzureRmSqlDatabaseGeoBackupPolicy;</span><span class="sxs-lookup"><span data-stu-id="94ce6-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="94ce6-157">Set-AzureRmSqlDatabaseGeoBackupPolicy.</span><span class="sxs-lookup"><span data-stu-id="94ce6-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="94ce6-158">Добавлены новые командлеты для API-интерфейсов помощников SQL Azure и рекомендуемых действий:</span><span class="sxs-lookup"><span data-stu-id="94ce6-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="94ce6-159">Get-AzureRmSqlDatabaseAdvisor;</span><span class="sxs-lookup"><span data-stu-id="94ce6-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="94ce6-160">Get-AzureRmSqlElasticPoolAdvisor;</span><span class="sxs-lookup"><span data-stu-id="94ce6-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="94ce6-161">Get-AzureRmSqlServerAdvisor;</span><span class="sxs-lookup"><span data-stu-id="94ce6-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="94ce6-162">Get-AzureRmSqlDatabaseRecommendedActions;</span><span class="sxs-lookup"><span data-stu-id="94ce6-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="94ce6-163">Get-AzureRmSqlElasticPoolRecommendedActions;</span><span class="sxs-lookup"><span data-stu-id="94ce6-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="94ce6-164">Get-AzureRmSqlServerRecommendedActions;</span><span class="sxs-lookup"><span data-stu-id="94ce6-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="94ce6-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus;</span><span class="sxs-lookup"><span data-stu-id="94ce6-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="94ce6-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus;</span><span class="sxs-lookup"><span data-stu-id="94ce6-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="94ce6-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus;</span><span class="sxs-lookup"><span data-stu-id="94ce6-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="94ce6-168">Set-AzureRmSqlDatabaseRecommendedActionState;</span><span class="sxs-lookup"><span data-stu-id="94ce6-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="94ce6-169">Set-AzureRmSqlElasticPoolRecommendedActionState;</span><span class="sxs-lookup"><span data-stu-id="94ce6-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="94ce6-170">Set-AzureRmSqlServerRecommendedActionState.</span><span class="sxs-lookup"><span data-stu-id="94ce6-170">Set-AzureRmSqlServerRecommendedActionState</span></span>