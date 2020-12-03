---
title: Обзор модуля администрирования PowerShell для Azure Stack | Документация Майкрософт
description: Обзор модуля администрирования PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: e19fea440025e7a00a037e360ac95ff8e0e62129
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96428016"
---
# <a name="azure-stack-module-180"></a>Модуль Azure Stack 1.8.0

## <a name="requirements"></a>Требования

Минимальная поддерживаемая версия Azure Stack — 1910.

Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).

## <a name="install"></a>Установка

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a>Заметки о выпуске

* Поддерживается в обновлении 1910.
* Внесенные изменения:

    - **Новый модуль администрирования DRP**. Поставщик ресурсов развертывания (DRP) поддерживает управляемые развертывания поставщиков ресурсов в Azure Stack Hub. Эти команды взаимодействуют со слоем Azure Resource Manager для взаимодействия с DRP.

    - **BRP**:
        - поддержка восстановления одной роли для резервного копирования инфраструктуры Azure Stack;
        - добавлен параметр `RoleName` в командлет R `estore-AzsBackup`.

    - **FRP**: критические изменения для ресурсов **диска** и **тома**, используемых с API версии 2019-05-01. Функции, поддерживаемые в Azure Stack Hub 1910 и более поздних версиях:
        - значения идентификатора `Name` `HealthStatus` и `OperationalStatus` были изменены;
        - включена поддержка новых свойств `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` и `StoragePool` для ресурсов **диска**;
        - свойства `CanPool` и `CannotPoolReason` ресурсов **диска** являются устаревшими; вместо них используйте `OperationalStatus`.