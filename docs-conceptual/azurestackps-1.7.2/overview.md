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
ms.openlocfilehash: 72974ac2fec42da962513c161c506e83f047bfb6
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427383"
---
# <a name="azure-stack-module-172"></a>Модуль Azure Stack 1.7.2

## <a name="requirements"></a>Требования

Минимальная поддерживаемая версия Azure Stack — 1904.

Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).

## <a name="install"></a>Установка

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a>Заметки о выпуске

* Поддерживается в обновлении 1904.
* Это критическое изменение выпуска. Дополнительные сведения о критических изменениях находятся по ссылке <https://aka.ms/azspshmigration170>.
* Критическое изменение. Изменения резервного копирования в режиме шифрования на основе сертификатов. Прекращена поддержка симметричных ключей.
* Дополнительные сведения о критических изменениях находятся по ссылке https://aka.ms/azspshmigration170.
* Модуль Azs.Storage.Admin 
* Исправления: новая квота хранилища использует значения по умолчанию, если значения отсутствуют.