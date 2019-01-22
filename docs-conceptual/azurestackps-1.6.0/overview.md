---
title: Обзор модуля администрирования PowerShell для Azure Stack | Документация Майкрософт
description: Обзор модуля администрирования PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 4e1174236796e7da929ff276addb32e42c18b707
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/12/2019
ms.locfileid: "54240141"
---
# <a name="azure-stack-module-160"></a>Модуль Azure Stack 1.6.0

## <a name="requirements"></a>Требования:
Минимальная поддерживаемая версия Azure Stack — 1811.

Примечание. Если вы используете более раннюю версию, установите версию 1.6.0.

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

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a>Заметки о выпуске
* Поддержка в обновлении 1811.
* Модуль Azs.Compute.Admin
    * Исправлен отсутствующий префикс Azs для объекта New-DataDiskObject, добавлен псевдоним с предупреждением о том, что в дальнейшем командлет будет отмечен как нерекомендуемый.
* Модуль Azs.Update.Admin:
    * Добавлено предупреждение с рекомендацией запускать Test-AzureStack перед установкой AzsUpdate.
* Azs.Fabric.Admin
    * Новый командлет (функции, поддерживаемые в Azure Stack 1811+):
        * Get-AzsDrive;
        * Get-AzsVolume;
        * Get-AzsStorageSubSystem.
    * Устаревшее
        * Get-AzsInfrastructureVolume — это псевдоним для командлета Get-AzsVolume.
* Azs.InfrastructureInsights.Admin
    *  Добавлен новый командлет Repair-AzsAlert.
* Azs.Storage.Admin:
    * Исправлена ошибка, возникающая, если значения квоты по умолчанию не используются.
* Модуль Azs.Subscriptions.Admin:
    * Исправлен отсутствующий префикс Azs для объекта New-AddonPlanDefinitionObject, добавлен псевдоним с предупреждением о том, что в дальнейшем командлет будет отмечен как нерекомендуемый.
