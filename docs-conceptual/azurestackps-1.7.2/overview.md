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
ms.openlocfilehash: b77e09f6fcd5b7752af9f51a42d357db4f1b13db
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037667"
---
# <a name="azure-stack-module-172"></a>Модуль Azure Stack 1.7.2

## <a name="requirements"></a>Требования:

Минимальная поддерживаемая версия Azure Stack — 1904.

Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).

## <a name="install"></a>Install

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
