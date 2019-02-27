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
ms.openlocfilehash: af34497f243ce8f4f718e88312f6ad54eb6ad848
ms.sourcegitcommit: 993db64e68b222acbcfdeef2e81eb3316b160858
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2019
ms.locfileid: "56240537"
---
# <a name="azure-stack-module-170"></a><span data-ttu-id="d3a10-103">Модуль Azure Stack 1.7.0</span><span class="sxs-lookup"><span data-stu-id="d3a10-103">Azure Stack Module 1.7.0</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a10-104">Требования:</span><span class="sxs-lookup"><span data-stu-id="d3a10-104">Requirements:</span></span>
<span data-ttu-id="d3a10-105">Минимальная поддерживаемая версия Azure Stack — 1901.</span><span class="sxs-lookup"><span data-stu-id="d3a10-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="d3a10-106">Примечание. Если вы используете более раннюю версию, установите версию 1.7.0.</span><span class="sxs-lookup"><span data-stu-id="d3a10-106">Note: If you are using an earlier version install version 1.7.0</span></span>

## <a name="install"></a><span data-ttu-id="d3a10-107">Install</span><span class="sxs-lookup"><span data-stu-id="d3a10-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.0
```
## <a name="release-notes"></a><span data-ttu-id="d3a10-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="d3a10-108">Release Notes</span></span>
* <span data-ttu-id="d3a10-109">Поддерживается в обновлении 1901.</span><span class="sxs-lookup"><span data-stu-id="d3a10-109">Supported with 1901 update</span></span>
* <span data-ttu-id="d3a10-110">Это критическое изменение выпуска.</span><span class="sxs-lookup"><span data-stu-id="d3a10-110">This a breaking change release.</span></span> <span data-ttu-id="d3a10-111">Дополнительные сведения о критических изменениях находятся по ссылке https://aka.ms/azspshmigration170.</span><span class="sxs-lookup"><span data-stu-id="d3a10-111">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="d3a10-112">Модуль Azs.Backup.Admin \* Критическое изменение: Изменения резервного копирования в режиме шифрования на основе сертификатов.</span><span class="sxs-lookup"><span data-stu-id="d3a10-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="d3a10-113">Прекращена поддержка симметричных ключей.</span><span class="sxs-lookup"><span data-stu-id="d3a10-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="d3a10-114">Модуль Azs.Fabric.Admin       \* Прекращение поддержки           \* Get-AzsInfrastructureVolume помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsVolume           \* Get-AzsStorageSystem помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsStorageSubSystem           \* Get-AzsStoragePool помечен как нерекомендуемый, объект StorageSubSystem имеет свойство емкости</span><span class="sxs-lookup"><span data-stu-id="d3a10-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="d3a10-115">Модуль Azs.Compute.Admin           \* Исправление ошибки: Add-AzsPlatformImage, Get-AzsPlatformImage — вызов ConvertTo-PlatformImageObject происходит только по правильному пути           \* Исправление ошибки: Add-AzsVmExtension, Get-AzsVmExtension — вызов ConvertTo-VmExtensionObject происходит только по правильному пути</span><span class="sxs-lookup"><span data-stu-id="d3a10-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="d3a10-116">Модуль Azs.Storage.Admin           \* Исправление ошибки: новая квота хранилища использует значения по умолчанию, если значения не указаны.</span><span class="sxs-lookup"><span data-stu-id="d3a10-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>

