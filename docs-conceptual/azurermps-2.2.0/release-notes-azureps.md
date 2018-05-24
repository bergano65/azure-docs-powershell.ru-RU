---
title: Журнал изменений Azure PowerShell | Документация Майкрософт
description: Это руководство содержит историю изменений Azure PowerShell, внесенных в новом выпуске.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 6fe226a2525142f82b894318b0588681bff0e2ef
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a><span data-ttu-id="a2035-103">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="a2035-103">Release notes</span></span>

<span data-ttu-id="a2035-104">Здесь приведен список изменений, внесенных в Azure PowerShell в этом выпуске.</span><span class="sxs-lookup"><span data-stu-id="a2035-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="a2035-105">Версия 2.2.0</span><span class="sxs-lookup"><span data-stu-id="a2035-105">Version 2.2.0</span></span>
* <span data-ttu-id="a2035-106">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="a2035-106">Compute</span></span>
  - <span data-ttu-id="a2035-107">Добавлена поддержка для запроса состояния шифрования из расширения AzureDiskEncryptionForLinux.</span><span class="sxs-lookup"><span data-stu-id="a2035-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="a2035-108">Фабрика данных</span><span class="sxs-lookup"><span data-stu-id="a2035-108">DataFactory</span></span>
  - <span data-ttu-id="a2035-109">Добавлен новый командлет для перечисления окон действий:</span><span class="sxs-lookup"><span data-stu-id="a2035-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="a2035-110">Get-AzureRmDataFactoryActivityWindow.</span><span class="sxs-lookup"><span data-stu-id="a2035-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="a2035-111">Data Lake</span><span class="sxs-lookup"><span data-stu-id="a2035-111">DataLake</span></span>
  - <span data-ttu-id="a2035-112">В следующих командлетах параметр `Host` изменен на `DatabaseHost`, а в `Host` добавлен псевдоним:</span><span class="sxs-lookup"><span data-stu-id="a2035-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="a2035-113">New-AzureRmDataLakeAnalyticsCatalogSecret;</span><span class="sxs-lookup"><span data-stu-id="a2035-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="a2035-114">Set-AzureRmDataLakeAnalyticsCatalogSecret.</span><span class="sxs-lookup"><span data-stu-id="a2035-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="a2035-115">Добавлена поддержка для удаления списка ACL и списка ACL по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a2035-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="a2035-116">Добавлена поддержка для получения и настройки разрешений без имени для файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="a2035-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="a2035-117">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="a2035-117">KeyVault</span></span>
  - <span data-ttu-id="a2035-118">Добавлена поддержка следующих сертификатов:</span><span class="sxs-lookup"><span data-stu-id="a2035-118">Add support for certificates</span></span>
    + <span data-ttu-id="a2035-119">Add-AzureKeyVaultCertificate;</span><span class="sxs-lookup"><span data-stu-id="a2035-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="a2035-120">Add-AzureKeyVaultCertificateContact;</span><span class="sxs-lookup"><span data-stu-id="a2035-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="a2035-121">Get-AzureKeyVaultCertificate;</span><span class="sxs-lookup"><span data-stu-id="a2035-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="a2035-122">Get-AzureKeyVaultCertificateContact;</span><span class="sxs-lookup"><span data-stu-id="a2035-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="a2035-123">Get-AzureKeyVaultCertificateIssuer;</span><span class="sxs-lookup"><span data-stu-id="a2035-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="a2035-124">Get-AzureKeyVaultCertificateOperation;</span><span class="sxs-lookup"><span data-stu-id="a2035-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="a2035-125">Get-AzureKeyVaultCertificatePolicy;</span><span class="sxs-lookup"><span data-stu-id="a2035-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="a2035-126">Import-AzureKeyVaultCertificate;</span><span class="sxs-lookup"><span data-stu-id="a2035-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="a2035-127">New-AzureKeyVaultCertificateAdministratorDetails;</span><span class="sxs-lookup"><span data-stu-id="a2035-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="a2035-128">New-AzureKeyVaultCertificateOrganizationDetails;</span><span class="sxs-lookup"><span data-stu-id="a2035-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="a2035-129">New-AzureKeyVaultCertificatePolicy;</span><span class="sxs-lookup"><span data-stu-id="a2035-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="a2035-130">Remove-AzureKeyVaultCertificate;</span><span class="sxs-lookup"><span data-stu-id="a2035-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="a2035-131">Remove-AzureKeyVaultCertificateContact;</span><span class="sxs-lookup"><span data-stu-id="a2035-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="a2035-132">Remove-AzureKeyVaultCertificateIssuer;</span><span class="sxs-lookup"><span data-stu-id="a2035-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="a2035-133">Remove-AzureKeyVaultCertificateOperation;</span><span class="sxs-lookup"><span data-stu-id="a2035-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="a2035-134">Set-AzureKeyVaultCertificateAttribute;</span><span class="sxs-lookup"><span data-stu-id="a2035-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="a2035-135">Set-AzureKeyVaultCertificateIssuer;</span><span class="sxs-lookup"><span data-stu-id="a2035-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="a2035-136">Set-AzureKeyVaultCertificatePolicy;</span><span class="sxs-lookup"><span data-stu-id="a2035-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="a2035-137">Stop-AzureKeyVaultCertificateOperation.</span><span class="sxs-lookup"><span data-stu-id="a2035-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="a2035-138">Сеть</span><span class="sxs-lookup"><span data-stu-id="a2035-138">Network</span></span>

  - <span data-ttu-id="a2035-139">Для сетевого интерфейса добавлен новый параметр переключателя, чтобы включить или отключить ускорение работы в сети — +New-AzureRmNetworkInterface -EnableAcceleratedNetworking.</span><span class="sxs-lookup"><span data-stu-id="a2035-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="a2035-140">Добавлены командлеты PowerShell для включения функций шлюза в режиме "активный-активный":</span><span class="sxs-lookup"><span data-stu-id="a2035-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="a2035-141">Add-AzureRmVirtualNetworkGatewayIpConfig;</span><span class="sxs-lookup"><span data-stu-id="a2035-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="a2035-142">Remove-AzureRmVirtualNetworkGatewayIpConfig.</span><span class="sxs-lookup"><span data-stu-id="a2035-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="a2035-143">Добавлен новый командлет:</span><span class="sxs-lookup"><span data-stu-id="a2035-143">Added new cmdlet</span></span>
    + <span data-ttu-id="a2035-144">Test-AzureRmPrivateIpAddressAvailability.</span><span class="sxs-lookup"><span data-stu-id="a2035-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="a2035-145">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="a2035-145">Resources</span></span>
  - <span data-ttu-id="a2035-146">Добавлена поддержка зон в командлетах поставщика и ресурсов:</span><span class="sxs-lookup"><span data-stu-id="a2035-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="a2035-147">Get-AzureRmProvider;</span><span class="sxs-lookup"><span data-stu-id="a2035-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="a2035-148">New-AzureRmResource;</span><span class="sxs-lookup"><span data-stu-id="a2035-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="a2035-149">Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="a2035-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="a2035-150">SQL</span><span class="sxs-lookup"><span data-stu-id="a2035-150">Sql</span></span>
  - <span data-ttu-id="a2035-151">Добавлены новые командлеты для управления политикой обнаружения угроз SQL Azure на уровне сервера:</span><span class="sxs-lookup"><span data-stu-id="a2035-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="a2035-152">Get-AzureRmSqlServerThreatDetectionPolicy;</span><span class="sxs-lookup"><span data-stu-id="a2035-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="a2035-153">Remove-AzureRmSqlServerThreatDetectionPolicy;</span><span class="sxs-lookup"><span data-stu-id="a2035-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="a2035-154">Set-AzureRmSqlServerThreatDetectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a2035-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="a2035-155">Добавлены новые командлеты для поддержки включения или отключения GeoBackupPolicy для Sql Azure DataWarehouses:</span><span class="sxs-lookup"><span data-stu-id="a2035-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="a2035-156">Get-AzureRmSqlDatabaseGeoBackupPolicy;</span><span class="sxs-lookup"><span data-stu-id="a2035-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="a2035-157">Set-AzureRmSqlDatabaseGeoBackupPolicy.</span><span class="sxs-lookup"><span data-stu-id="a2035-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="a2035-158">Добавлены новые командлеты для API-интерфейсов помощников SQL Azure и рекомендуемых действий:</span><span class="sxs-lookup"><span data-stu-id="a2035-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="a2035-159">Get-AzureRmSqlDatabaseAdvisor;</span><span class="sxs-lookup"><span data-stu-id="a2035-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="a2035-160">Get-AzureRmSqlElasticPoolAdvisor;</span><span class="sxs-lookup"><span data-stu-id="a2035-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="a2035-161">Get-AzureRmSqlServerAdvisor;</span><span class="sxs-lookup"><span data-stu-id="a2035-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="a2035-162">Get-AzureRmSqlDatabaseRecommendedActions;</span><span class="sxs-lookup"><span data-stu-id="a2035-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="a2035-163">Get-AzureRmSqlElasticPoolRecommendedActions;</span><span class="sxs-lookup"><span data-stu-id="a2035-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="a2035-164">Get-AzureRmSqlServerRecommendedActions;</span><span class="sxs-lookup"><span data-stu-id="a2035-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="a2035-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus;</span><span class="sxs-lookup"><span data-stu-id="a2035-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="a2035-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus;</span><span class="sxs-lookup"><span data-stu-id="a2035-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="a2035-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus;</span><span class="sxs-lookup"><span data-stu-id="a2035-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="a2035-168">Set-AzureRmSqlDatabaseRecommendedActionState;</span><span class="sxs-lookup"><span data-stu-id="a2035-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="a2035-169">Set-AzureRmSqlElasticPoolRecommendedActionState;</span><span class="sxs-lookup"><span data-stu-id="a2035-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="a2035-170">Set-AzureRmSqlServerRecommendedActionState.</span><span class="sxs-lookup"><span data-stu-id="a2035-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
