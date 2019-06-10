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
# <a name="azure-stack-module-172"></a>Модуль Azure Stack 1.7.2

## <a name="requirements"></a>Требования:

Минимальная поддерживаемая версия Azure Stack — 1904.

Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).

## <a name="install-powershell-for-azure-stack"></a>Установка PowerShell для Azure Stack

Установка происходит в три этапа.

1. Установка PowerShell для Azure Stack в зависимости от версии Azure Stack
2. Включение дополнительных возможностей хранилища
3. Подтверждение установки PowerShell

### <a name="install-azure-stack-powershell"></a>Установка PowerShell для Azure Stack

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

### <a name="enable-additional-storage-features"></a>Включение дополнительных возможностей хранилища

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

## <a name="release-notes"></a>Заметки о выпуске

* Поддерживается в обновлении 1904.
* Это критическое изменение выпуска. Дополнительные сведения о критических изменениях находятся по ссылке <https://aka.ms/azspshmigration170>.
* Модуль Azs.Backup.Admin * Критическое изменение: Изменения резервного копирования в режиме шифрования на основе сертификатов. Прекращена поддержка симметричных ключей.
* Модуль Azs.Fabric.Admin       * Прекращение поддержки           * Get-AzsInfrastructureVolume помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsVolume           * Get-AzsStorageSystem помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsStorageSubSystem           * Get-AzsStoragePool помечен как нерекомендуемый, объект StorageSubSystem имеет свойство емкости
* Модуль Azs.Compute.Admin           * Исправление ошибки: Add-AzsPlatformImage, Get-AzsPlatformImage — вызов ConvertTo-PlatformImageObject происходит только по правильному пути           * Исправление ошибки: Add-AzsVmExtension, Get-AzsVmExtension — вызов ConvertTo-VmExtensionObject происходит только по правильному пути
* Модуль Azs.Storage.Admin           * Исправление ошибки: новая квота хранилища использует значения по умолчанию, если значения не указаны.
