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
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/18/2019
ms.locfileid: "58808066"
---
# <a name="azure-stack-module-171"></a>Модуль Azure Stack 1.7.1

## <a name="requirements"></a>Требования:

Минимальная поддерживаемая версия Azure Stack — 1901.

Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).

## <a name="install"></a>Install

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a>Заметки о выпуске

* Поддерживается в обновлении 1901.
* Это критическое изменение выпуска. Дополнительные сведения о критических изменениях находятся по ссылке <https://aka.ms/azspshmigration170>.
* Модуль Azs.Backup.Admin * Критическое изменение: Изменения резервного копирования в режиме шифрования на основе сертификатов. Прекращена поддержка симметричных ключей.
* Модуль Azs.Fabric.Admin       * Прекращение поддержки           * Get-AzsInfrastructureVolume помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsVolume           * Get-AzsStorageSystem помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsStorageSubSystem           * Get-AzsStoragePool помечен как нерекомендуемый, объект StorageSubSystem имеет свойство емкости
* Модуль Azs.Compute.Admin           * Исправление ошибки: Add-AzsPlatformImage, Get-AzsPlatformImage — вызов ConvertTo-PlatformImageObject происходит только по правильному пути           * Исправление ошибки: Add-AzsVmExtension, Get-AzsVmExtension — вызов ConvertTo-VmExtensionObject происходит только по правильному пути
* Модуль Azs.Storage.Admin           * Исправление ошибки: новая квота хранилища использует значения по умолчанию, если значения не указаны.
