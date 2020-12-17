---
title: Обзор модуля администрирования PowerShell для Azure Stack Hub | Документация Майкрософт
description: Обзор модуля администрирования PowerShell Azure Stack Hub с инструкциями по установке и настройке.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: ec4591e4f44fa56b7482d2dec3f525cb02dbd94b
ms.sourcegitcommit: a24069b411d3a6011067770430b6dcdd4b2c2159
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/16/2020
ms.locfileid: "97532265"
---
# <a name="azure-stack-hub-module-202"></a>Модуль Azure Stack Hub 2.0.2

## <a name="requirements"></a>Требования

Минимальная поддерживаемая версия Azure Stack Hub — 2002.

Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).

## <a name="install"></a>Установка

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease -SkipPublisherCheck

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a>Заметки о выпуске

* Поддерживается в обновлении 2002.  

  Модуль Azure Stack Hub версии 2.0.0 является критическим изменением. Модуль использует модуль Az, а не модуль AzureRM. См. [список критических изменений и руководство по миграции из AzureRM в Az Azure PowerShell в Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).
