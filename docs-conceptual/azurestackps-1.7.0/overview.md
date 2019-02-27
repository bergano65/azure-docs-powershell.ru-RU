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
# <a name="azure-stack-module-170"></a>Модуль Azure Stack 1.7.0

## <a name="requirements"></a>Требования:
Минимальная поддерживаемая версия Azure Stack — 1901.

Примечание. Если вы используете более раннюю версию, установите версию 1.7.0.

## <a name="install"></a>Install
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
## <a name="release-notes"></a>Заметки о выпуске
* Поддерживается в обновлении 1901.
* Это критическое изменение выпуска. Дополнительные сведения о критических изменениях находятся по ссылке https://aka.ms/azspshmigration170.
* Модуль Azs.Backup.Admin * Критическое изменение: Изменения резервного копирования в режиме шифрования на основе сертификатов. Прекращена поддержка симметричных ключей.
* Модуль Azs.Fabric.Admin       * Прекращение поддержки           * Get-AzsInfrastructureVolume помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsVolume           * Get-AzsStorageSystem помечен как нерекомендуемый, мы предоставляем новый командлет Get-AzsStorageSubSystem           * Get-AzsStoragePool помечен как нерекомендуемый, объект StorageSubSystem имеет свойство емкости
* Модуль Azs.Compute.Admin           * Исправление ошибки: Add-AzsPlatformImage, Get-AzsPlatformImage — вызов ConvertTo-PlatformImageObject происходит только по правильному пути           * Исправление ошибки: Add-AzsVmExtension, Get-AzsVmExtension — вызов ConvertTo-VmExtensionObject происходит только по правильному пути
* Модуль Azs.Storage.Admin           * Исправление ошибки: новая квота хранилища использует значения по умолчанию, если значения не указаны.

