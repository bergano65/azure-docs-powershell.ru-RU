---
title: Обзор модуля администрирования PowerShell для Azure Stack | Документация Майкрософт
description: Обзор модуля администрирования PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855794"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="9f02b-103">Модуль Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="9f02b-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="9f02b-104">Требования:</span><span class="sxs-lookup"><span data-stu-id="9f02b-104">Requirements:</span></span>

<span data-ttu-id="9f02b-105">Минимальная поддерживаемая версия Azure Stack — 1904.</span><span class="sxs-lookup"><span data-stu-id="9f02b-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="9f02b-106">Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="9f02b-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="9f02b-107">Установка PowerShell для Azure Stack</span><span class="sxs-lookup"><span data-stu-id="9f02b-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="9f02b-108">Установка происходит в три этапа.</span><span class="sxs-lookup"><span data-stu-id="9f02b-108">Installation has three steps:</span></span>

1. <span data-ttu-id="9f02b-109">Установка PowerShell для Azure Stack в зависимости от версии Azure Stack</span><span class="sxs-lookup"><span data-stu-id="9f02b-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="9f02b-110">Включение дополнительных возможностей хранилища</span><span class="sxs-lookup"><span data-stu-id="9f02b-110">Enable additional storage features</span></span>
3. <span data-ttu-id="9f02b-111">Подтверждение установки PowerShell</span><span class="sxs-lookup"><span data-stu-id="9f02b-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="9f02b-112">Установка PowerShell для Azure Stack</span><span class="sxs-lookup"><span data-stu-id="9f02b-112">Install Azure Stack PowerShell</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a><span data-ttu-id="9f02b-113">Включение дополнительных возможностей хранилища</span><span class="sxs-lookup"><span data-stu-id="9f02b-113">Enable additional storage features</span></span>

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a><span data-ttu-id="9f02b-114">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="9f02b-114">Release Notes</span></span>

* <span data-ttu-id="9f02b-115">Поддерживается в обновлении 1904.</span><span class="sxs-lookup"><span data-stu-id="9f02b-115">Supported with 1904 update</span></span>
* <span data-ttu-id="9f02b-116">Это критическое изменение выпуска.</span><span class="sxs-lookup"><span data-stu-id="9f02b-116">This a breaking change release.</span></span> <span data-ttu-id="9f02b-117">Дополнительные сведения о критических изменениях находятся по ссылке <https://aka.ms/azspshmigration170>.</span><span class="sxs-lookup"><span data-stu-id="9f02b-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="9f02b-118">Модуль Azs.Backup.Admin \* Критическое изменение: Изменения резервного копирования в режиме шифрования на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="9f02b-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="9f02b-119">Прекращена поддержка симметричных ключей.</span><span class="sxs-lookup"><span data-stu-id="9f02b-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="9f02b-120">Модуль Azs.Fabric.Admin       \* Прекращение поддержки           \* Get-AzsInfrastructureVolume помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsVolume           \* Get-AzsStorageSystem помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsStorageSubSystem           \* Get-AzsStoragePool помечен как нерекомендуемый, объект StorageSubSystem имеет свойство емкости</span><span class="sxs-lookup"><span data-stu-id="9f02b-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="9f02b-121">Модуль Azs.Compute.Admin           \* Исправление ошибки: Add-AzsPlatformImage, Get-AzsPlatformImage — вызов ConvertTo-PlatformImageObject происходит только по правильному пути           \* Исправление ошибки: Add-AzsVmExtension, Get-AzsVmExtension — вызов ConvertTo-VmExtensionObject происходит только по правильному пути</span><span class="sxs-lookup"><span data-stu-id="9f02b-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="9f02b-122">Модуль Azs.Storage.Admin           \* Исправление ошибки: новая квота хранилища использует значения по умолчанию, если значения не указаны.</span><span class="sxs-lookup"><span data-stu-id="9f02b-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
