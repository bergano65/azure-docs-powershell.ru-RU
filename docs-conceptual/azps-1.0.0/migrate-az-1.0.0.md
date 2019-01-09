---
title: Критические изменения в Microsoft Azure PowerShell Az 1.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Az версии 1 в Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2018
ms.locfileid: "53595211"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="5ede0-103">Руководство по миграции для Az версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="5ede0-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="5ede0-104">Этот документ описывает изменения между AzureRM версии 6.x и Az версии 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="5ede0-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="5ede0-105">Оглавление</span><span class="sxs-lookup"><span data-stu-id="5ede0-105">Table of Contents</span></span>
- [<span data-ttu-id="5ede0-106">Общие критически важные изменения</span><span class="sxs-lookup"><span data-stu-id="5ede0-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="5ede0-107">Изменения префикса существительного командлета</span><span class="sxs-lookup"><span data-stu-id="5ede0-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="5ede0-108">Изменение имени модуля</span><span class="sxs-lookup"><span data-stu-id="5ede0-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="5ede0-109">Удаленные модули</span><span class="sxs-lookup"><span data-stu-id="5ede0-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="5ede0-110">Windows PowerShell 5.1 и .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="5ede0-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="5ede0-111">Временное удаление входа пользователя с помощью PSCredential</span><span class="sxs-lookup"><span data-stu-id="5ede0-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="5ede0-112">Вход с кодом устройства по умолчанию вместо запроса веб-браузера</span><span class="sxs-lookup"><span data-stu-id="5ede0-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="5ede0-113">Критические изменения модуля</span><span class="sxs-lookup"><span data-stu-id="5ede0-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="5ede0-114">Az.ApiManagement (ранее AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="5ede0-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="5ede0-115">Az.Billing (ранее AzureRM.Billing, AzureRM.Consitation и AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="5ede0-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="5ede0-116">Az.CognitiveServices (ранее AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="5ede0-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="5ede0-117">Az.Compute (ранее AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="5ede0-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="5ede0-118">Az.DataFactory (ранее AzureRM.DataFactories и AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="5ede0-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="5ede0-119">Az.DataLakeAnalytics (ранее AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="5ede0-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="5ede0-120">Az.DataLakeStore (ранее AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="5ede0-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="5ede0-121">Az.KeyVault (ранее AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="5ede0-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="5ede0-122">Az.Media (ранее AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="5ede0-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="5ede0-123">Az.Monitor (ранее AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="5ede0-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="5ede0-124">Az.Network (ранее AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="5ede0-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="5ede0-125">Az.OperationalInsights (ранее AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="5ede0-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="5ede0-126">Az.RecoveryServices (ранее AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup и AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="5ede0-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="5ede0-127">Az.Resources (ранее AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="5ede0-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="5ede0-128">Az.ServiceFabric (ранее AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="5ede0-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="5ede0-129">Az.Sql (ранее AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="5ede0-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="5ede0-130">Az.Storage (ранее Azure.Storage и AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="5ede0-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="5ede0-131">Az.Websites (ранее AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="5ede0-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="5ede0-132">Общие критически важные изменения</span><span class="sxs-lookup"><span data-stu-id="5ede0-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="5ede0-133">Изменения префикса существительного командлета</span><span class="sxs-lookup"><span data-stu-id="5ede0-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="5ede0-134">В AzureRM командлеты использовали либо "AzureRM", либо "Azure" в качестве префикса существительного.</span><span class="sxs-lookup"><span data-stu-id="5ede0-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="5ede0-135">Az упрощает и нормализует имена командлетов, так что все командлеты используют "Az" в качестве префикса существительного командлета.</span><span class="sxs-lookup"><span data-stu-id="5ede0-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="5ede0-136">Например: </span><span class="sxs-lookup"><span data-stu-id="5ede0-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="5ede0-137">Изменено на</span><span class="sxs-lookup"><span data-stu-id="5ede0-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="5ede0-138">Чтобы упростить переход на эти новые имена командлетов, Az представляет два новых командлета: ```Enable-AzureRmAlias``` и ```Disable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="5ede0-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="5ede0-139">```Enable-AzureRmAlias``` создает псевдонимы из старых имен командлетов в AzureRM для новых имен командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="5ede0-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="5ede0-140">Командлет позволяет создавать псевдонимы в текущем сеансе или во всех сеансах путем изменения профиля пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="5ede0-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="5ede0-141">Следующий сценарий в AzureRM является примером.</span><span class="sxs-lookup"><span data-stu-id="5ede0-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="5ede0-142">Его можно выполнить с минимальными изменениями с помощью ```Enable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="5ede0-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="5ede0-143">Выполнение ```Enable-AzureRmAlias -Scope CurrentUser``` включит псевдонимы для всех открытых сеансов PowerShell, так что после выполнения этого командлета такой сценарий вообще не нужно будет изменять.</span><span class="sxs-lookup"><span data-stu-id="5ede0-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="5ede0-144">Для получения дополнительных сведений об использовании командлетов псевдонимов выполните ```Get-Help -Online Enable-AzureRmAlias``` в командной строке PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ede0-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="5ede0-145">```Disable-AzureRmAlias``` удаляет псевдонимы командлетов AzureRM, созданные ```Enable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="5ede0-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="5ede0-146">Для получения дополнительных сведений выполните ```Get-Help -Online Disable-AzureRmAlias``` в командной строке PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ede0-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="5ede0-147">Изменение имени модуля</span><span class="sxs-lookup"><span data-stu-id="5ede0-147">Module Name Changes</span></span>
- <span data-ttu-id="5ede0-148">Имена модулей изменены с `AzureRM.*` на `Az.*`, за исключением следующих модулей.</span><span class="sxs-lookup"><span data-stu-id="5ede0-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="5ede0-149">Изменения в именах модулей означают, что любой сценарий, который использует ```#Requires``` или ```Import-Module``` для загрузки определенных модулей, необходимо будет изменить, чтобы вместо него использовать новый модуль.</span><span class="sxs-lookup"><span data-stu-id="5ede0-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="5ede0-150">Миграция операторов #Requires</span><span class="sxs-lookup"><span data-stu-id="5ede0-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="5ede0-151">Сценарии, использующие #Requires для объявления зависимости от модулей AzureRM, должны быть обновлены для использования новых имен модулей.</span><span class="sxs-lookup"><span data-stu-id="5ede0-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="5ede0-152">Следует изменить на</span><span class="sxs-lookup"><span data-stu-id="5ede0-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="5ede0-153">Миграция операторов Import-Module</span><span class="sxs-lookup"><span data-stu-id="5ede0-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="5ede0-154">Сценарии, которые используют ```Import-Module``` для загрузки модулей AzureRM, необходимо обновить, чтобы отразились новые имена модулей.</span><span class="sxs-lookup"><span data-stu-id="5ede0-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="5ede0-155">Следует изменить на</span><span class="sxs-lookup"><span data-stu-id="5ede0-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="5ede0-156">Миграция вызовов командлета Fully-Qualified</span><span class="sxs-lookup"><span data-stu-id="5ede0-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="5ede0-157">Сценарии, использующие квалифицированные вызовы командлетов, ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="5ede0-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="5ede0-158">Следует изменить, чтобы использовать новые имена модулей и командлетов.</span><span class="sxs-lookup"><span data-stu-id="5ede0-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="5ede0-159">Миграция зависимостей манифеста модуля</span><span class="sxs-lookup"><span data-stu-id="5ede0-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="5ede0-160">Модули, которые выражают зависимости от модулей AzureRM через файл манифеста модуля (.psd1), должны обновить имена модулей в разделе "RequiredModules".</span><span class="sxs-lookup"><span data-stu-id="5ede0-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="5ede0-161">Следует изменить на</span><span class="sxs-lookup"><span data-stu-id="5ede0-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="5ede0-162">Удаленные модули</span><span class="sxs-lookup"><span data-stu-id="5ede0-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="5ede0-163">Средства для работы с этими службами больше не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="5ede0-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="5ede0-164">Клиентам рекомендуется обратиться к альтернативным службам, как только появится возможность.</span><span class="sxs-lookup"><span data-stu-id="5ede0-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="5ede0-165">Windows PowerShell 5.1 и .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="5ede0-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="5ede0-166">Для использования Az с Windows PowerShell 5.1 требуется установка .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="5ede0-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="5ede0-167">Тем не менее для использования Az с PowerShell Core не требуется .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="5ede0-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="5ede0-168">Временное удаление входа пользователя с помощью PSCredential</span><span class="sxs-lookup"><span data-stu-id="5ede0-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="5ede0-169">Из-за изменений в процессе проверки подлинности для .NET Standard мы временно удаляем вход пользователя через PSCredential.</span><span class="sxs-lookup"><span data-stu-id="5ede0-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="5ede0-170">Эта возможность будет доступна в выпуске от 15 января 2019 г. для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="5ede0-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="5ede0-171">Это подробно описано [здесь.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="5ede0-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="5ede0-172">Вход с кодом устройства по умолчанию вместо запроса веб-браузера</span><span class="sxs-lookup"><span data-stu-id="5ede0-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="5ede0-173">Из-за изменений в процессе проверки подлинности для .NET Standard мы используем вход устройства в качестве потока входа по умолчанию во время интерактивного входа.</span><span class="sxs-lookup"><span data-stu-id="5ede0-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="5ede0-174">Вход через веб-браузер будет повторно представлен для Windows PowerShell 5.1 в качестве версии по умолчанию в выпуске от 15 января 2019 г.</span><span class="sxs-lookup"><span data-stu-id="5ede0-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="5ede0-175">В это время пользователи смогут выбрать вход устройства с помощью параметра Switch.</span><span class="sxs-lookup"><span data-stu-id="5ede0-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="5ede0-176">Критические изменения модуля</span><span class="sxs-lookup"><span data-stu-id="5ede0-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="5ede0-177">Az.ApiManagement (ранее AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="5ede0-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="5ede0-178">Удаление приведенных ниже командлетов.</span><span class="sxs-lookup"><span data-stu-id="5ede0-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="5ede0-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ede0-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="5ede0-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="5ede0-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="5ede0-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="5ede0-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="5ede0-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="5ede0-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="5ede0-183">Используйте командлет **Set-AzApiManagement**, чтобы установить эти свойства</span><span class="sxs-lookup"><span data-stu-id="5ede0-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="5ede0-184">Следующие свойства были удалены.</span><span class="sxs-lookup"><span data-stu-id="5ede0-184">Following properties were removed</span></span>
  - <span data-ttu-id="5ede0-185">Удалены свойства: `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` и `ScmHostnameConfiguration` типа `PsApiManagementHostnameConfiguration` из `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="5ede0-186">Вместо этого используйте: `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` и `ScmCustomHostnameConfiguration` типа `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="5ede0-187">Свойство `StaticIPs` удалено из PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5ede0-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="5ede0-188">Свойство было разделено на `PublicIPAddresses` и `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="5ede0-189">Обязательное свойство `Location` удалено из командлета New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="5ede0-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="5ede0-190">Az.Billing (ранее AzureRM.Billing, AzureRM.Consitation и AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="5ede0-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="5ede0-191">Параметр `InvoiceName` удален из командлета `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="5ede0-192">Для сценариев необходимо использовать другие параметры идентификации для счета.</span><span class="sxs-lookup"><span data-stu-id="5ede0-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="5ede0-193">Az.CognitiveServices (ранее AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="5ede0-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="5ede0-194">Набор параметров `GetSkusWithAccountParamSetName` удален из командлета `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="5ede0-195">Необходимо получить Skus по типу и расположению учетной записи, а не использовать ResourceGroupName и имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5ede0-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="5ede0-196">Az.Compute (ранее AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="5ede0-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="5ede0-197">`IdentityIds` удалены из свойства `Identity` в объектах `PSVirtualMachine` и `PSVirtualMachineScaleSet`. Сценарии больше не должны использовать значение этого поля для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="5ede0-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="5ede0-198">Тип свойства `InstanceView` объекта `PSVirtualMachineScaleSetVM` изменен с `VirtualMachineInstanceView` на `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="5ede0-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="5ede0-199">Свойства `AutoOSUpgradePolicy` и `AutomaticOSUpgrade` удалены из свойства `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="5ede0-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="5ede0-200">Тип свойства `Sku` в объекте `PSSnapshotUpdate` изменен с `DiskSku` на `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="5ede0-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="5ede0-201">`VmScaleSetVMParameterSet` удалено из командлета `Add-AzVMDataDisk`, вы больше не можете отдельно добавлять диск с данными в виртуальную машину масштабируемого набора.</span><span class="sxs-lookup"><span data-stu-id="5ede0-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="5ede0-202">Az.DataFactory (ранее AzureRM.DataFactories и AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="5ede0-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="5ede0-203">Параметр `GatewayName` стал обязательным в командлете `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="5ede0-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="5ede0-204">Командлет `New-AzDataFactoryGatewayKey` удалено</span><span class="sxs-lookup"><span data-stu-id="5ede0-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="5ede0-205">Параметр `LinkedServiceName` удален из командлета `Get-AzDataFactoryV2ActivityRun`. Сценарии больше не должны использовать значение этого поля для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="5ede0-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="5ede0-206">Az.DataLakeAnalytics (ранее AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="5ede0-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="5ede0-207">Удалены следующие нерекомендуемые командлеты: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` и `Set-AzDataLakeAnalyticsCatalogSecret`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="5ede0-208">Az.DataLakeStore (ранее AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="5ede0-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="5ede0-209">В следующих командлетах параметр `Encoding` изменен с типа `FileSystemCmdletProviderEncoding` на `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="5ede0-210">Это изменение удаляет значения кодирования `String` и `Oem`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="5ede0-211">Все остальные предыдущие значения кодирования остаются.</span><span class="sxs-lookup"><span data-stu-id="5ede0-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="5ede0-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5ede0-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="5ede0-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="5ede0-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="5ede0-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="5ede0-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="5ede0-215">Удален нерекомендуемый псевдоним свойства `Tags` из командлетов `New-AzDataLakeStoreAccount` и `Set-AzDataLakeStoreAccount`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="5ede0-216">Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="5ede0-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="5ede0-217">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="5ede0-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="5ede0-218">Из объекта ```PSDataLakeStoreAccountBasic``` удалены нерекомендуемые свойства: ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps```.</span><span class="sxs-lookup"><span data-stu-id="5ede0-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="5ede0-219">Любой сценарий, который использует ```PSDatalakeStoreAccount```, возвращенный из ```Get-AzDataLakeStoreAccount```, не должен ссылаться на эти свойства.</span><span class="sxs-lookup"><span data-stu-id="5ede0-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="5ede0-220">Az.KeyVault (ранее AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="5ede0-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="5ede0-221">Свойство `PurgeDisabled` было удалено из объектов `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` и `PSKeyVaultSecretAttributes`. Сценарии больше не должны ссылаться на свойство ```PurgeDisabled``` для принятия решений об обработке.</span><span class="sxs-lookup"><span data-stu-id="5ede0-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="5ede0-222">Az.Media (ранее AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="5ede0-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="5ede0-223">Удалите нерекомендуемый псевдоним свойства `Tags` из командлета `New-AzMediaService`. Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="5ede0-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="5ede0-224">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="5ede0-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="5ede0-225">Az.Monitor (ранее AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="5ede0-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="5ede0-226">Множественные имена `Categories` и `Timegrains` параметра удалены в пользу единичных имен параметров из командлета `Set-AzDiagnosticSetting`. Сценарии, которые используют</span><span class="sxs-lookup"><span data-stu-id="5ede0-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="5ede0-227">следует изменить на</span><span class="sxs-lookup"><span data-stu-id="5ede0-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="5ede0-228">Az.Network (ранее AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="5ede0-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="5ede0-229">Из командлета `Get-AzServiceEndpointPolicyDefinition` удален нерекомендуемый параметр `ResourceId`</span><span class="sxs-lookup"><span data-stu-id="5ede0-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="5ede0-230">Из объекта `PSVirtualNetwork` удалено нерекомендуемое свойство `EnableVmProtection`</span><span class="sxs-lookup"><span data-stu-id="5ede0-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="5ede0-231">Нерекомендуемый командлет `Set-AzVirtualNetworkGatewayVpnClientConfig` удален</span><span class="sxs-lookup"><span data-stu-id="5ede0-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="5ede0-232">Сценарии больше не должны принимать решения об обработке на основе значений этих полей.</span><span class="sxs-lookup"><span data-stu-id="5ede0-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="5ede0-233">Az.OperationalInsights (ранее AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="5ede0-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="5ede0-234">Набор параметров по умолчанию для `Get-AzOperationalInsightsDataSource` удален и заменен на `ByWorkspaceNameByKind`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="5ede0-235">Сценарии, в которых перечислены источники данных, использующие</span><span class="sxs-lookup"><span data-stu-id="5ede0-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="5ede0-236">следует изменить, чтобы указать вид</span><span class="sxs-lookup"><span data-stu-id="5ede0-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="5ede0-237">Az.RecoveryServices (ранее AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup и AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="5ede0-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="5ede0-238">Из командлета `New/Set-AzRecoveryServicesAsrPolicy` удален параметр `Encryption`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="5ede0-239">Параметр `TargetStorageAccountName` теперь является обязательным для восстановления управляемого диска в командлете `Restore-AzRecoveryServicesBackupItem`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="5ede0-240">В командлете `Restore-AzRecoveryServicesBackupItem` удалены параметры `StorageAccountName` и `StorageAccountResourceGroupName`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="5ede0-241">В командлете `Get-AzRecoveryServicesBackupContainer` удален параметр `Name`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="5ede0-242">Az.Resources (ранее AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="5ede0-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="5ede0-243">Из командлета `New/Set-AzPolicyAssignment` удален параметр `Sku`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="5ede0-244">Параметр `Password` удален из командлетов `New-AzADServicePrincipal` и `New-AzADSpCredential`. Пароли генерируются автоматически. Сценарии, которые предоставили пароль:</span><span class="sxs-lookup"><span data-stu-id="5ede0-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="5ede0-245">следует изменить, чтобы получить пароль из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5ede0-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="5ede0-246">Az.ServiceFabric (ранее AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="5ede0-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="5ede0-247">Следующие типы возвращаемого значения командлета были изменены.</span><span class="sxs-lookup"><span data-stu-id="5ede0-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="5ede0-248">Свойство `SerivceTypeHealthPolicies` типа `ApplicationHealthPolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="5ede0-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="5ede0-249">Свойство `ApplicationHealthPolicies` типа `ClusterUpgradeDeltaHealthPolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="5ede0-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="5ede0-250">Свойство `OverrideUserUpgradePolicy` типа `ClusterUpgradePolicy` удалено.</span><span class="sxs-lookup"><span data-stu-id="5ede0-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="5ede0-251">Эти изменения влияют на следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="5ede0-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="5ede0-252">Add-AzServiceFabricClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="5ede0-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="5ede0-253">Add-AzServiceFabricClusterCertificate;</span><span class="sxs-lookup"><span data-stu-id="5ede0-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="5ede0-254">Add-AzServiceFabricNode;</span><span class="sxs-lookup"><span data-stu-id="5ede0-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="5ede0-255">Add-AzServiceFabricNodeType;</span><span class="sxs-lookup"><span data-stu-id="5ede0-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="5ede0-256">Get-AzServiceFabricCluster;</span><span class="sxs-lookup"><span data-stu-id="5ede0-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="5ede0-257">Remove-AzServiceFabricClientCertificate;</span><span class="sxs-lookup"><span data-stu-id="5ede0-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="5ede0-258">Remove-AzServiceFabricClusterCertificate;</span><span class="sxs-lookup"><span data-stu-id="5ede0-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="5ede0-259">Remove-AzServiceFabricNode;</span><span class="sxs-lookup"><span data-stu-id="5ede0-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="5ede0-260">Remove-AzServiceFabricNodeType;</span><span class="sxs-lookup"><span data-stu-id="5ede0-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="5ede0-261">Remove-AzServiceFabricSetting;</span><span class="sxs-lookup"><span data-stu-id="5ede0-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="5ede0-262">Set-AzServiceFabricSetting;</span><span class="sxs-lookup"><span data-stu-id="5ede0-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="5ede0-263">Set-AzServiceFabricUpgradeType;</span><span class="sxs-lookup"><span data-stu-id="5ede0-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="5ede0-264">Update-AzServiceFabricDurability;</span><span class="sxs-lookup"><span data-stu-id="5ede0-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="5ede0-265">Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="5ede0-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="5ede0-266">Az.Sql (ранее AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="5ede0-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="5ede0-267">Из командлета `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` удалены параметры `State` и `ResourceId`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="5ede0-268">Удалены следующие нерекомендуемые командлеты: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="5ede0-269">Из командлета `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` удален нерекомендуемый параметр `Current`</span><span class="sxs-lookup"><span data-stu-id="5ede0-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="5ede0-270">Из командлета `Get-AzSqlServerServiceObjective` удален нерекомендуемый параметр `DatabaseName`</span><span class="sxs-lookup"><span data-stu-id="5ede0-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="5ede0-271">Из командлета `Set-AzSqlDatabaseDataMaskingPolicy` удален нерекомендуемый параметр `PrivilegedLogin`</span><span class="sxs-lookup"><span data-stu-id="5ede0-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="5ede0-272">Az.Storage (ранее Azure.Storage и AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="5ede0-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="5ede0-273">Для поддержки создания контекста хранения Oauth только с именем учетной записи хранения набор параметров по умолчанию был изменен на `OAuthParameterSet`.</span><span class="sxs-lookup"><span data-stu-id="5ede0-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="5ede0-274">Пример: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="5ede0-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="5ede0-275">Параметр `Location` стал обязательным в командлете `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="5ede0-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="5ede0-276">Методы API службы хранилища теперь используют асинхронную модель на основе задач (TAP) вместо синхронных вызовов API.</span><span class="sxs-lookup"><span data-stu-id="5ede0-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="5ede0-277">1. Моментальный снимок большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="5ede0-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="5ede0-278">До:</span><span class="sxs-lookup"><span data-stu-id="5ede0-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="5ede0-279">После:</span><span class="sxs-lookup"><span data-stu-id="5ede0-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="5ede0-280">2. Общий доступ к снимку</span><span class="sxs-lookup"><span data-stu-id="5ede0-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="5ede0-281">До:</span><span class="sxs-lookup"><span data-stu-id="5ede0-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="5ede0-282">После:</span><span class="sxs-lookup"><span data-stu-id="5ede0-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="5ede0-283">3. Отмена обратимого удаления большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="5ede0-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="5ede0-284">До:</span><span class="sxs-lookup"><span data-stu-id="5ede0-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="5ede0-285">После:</span><span class="sxs-lookup"><span data-stu-id="5ede0-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="5ede0-286">4. Установка уровня большого двоичного объекта</span><span class="sxs-lookup"><span data-stu-id="5ede0-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="5ede0-287">До:</span><span class="sxs-lookup"><span data-stu-id="5ede0-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="5ede0-288">После:</span><span class="sxs-lookup"><span data-stu-id="5ede0-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="5ede0-289">Az.Websites (ранее AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="5ede0-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="5ede0-290">Из объектов `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` и `PSSite` удалены нерекомендуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5ede0-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>