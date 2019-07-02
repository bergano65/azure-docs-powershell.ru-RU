---
title: Общие сведения об Azure PowerShell
description: Общие сведения об установке и начале работы с модулем Az для Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 710decaf8fcc0ba57e1e978a665474047393adc7
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516629"
---
# <a name="overview-of-azure-powershell"></a>Общие сведения об Azure PowerShell

В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure. Azure PowerShell использует .NET Standard, делая его доступным для Windows, macOS и Linux.
Среда Azure PowerShell также доступна в Azure Cloud Shell.

## <a name="about-the-new-az-module"></a>Сведения о новом модуле Az

В этой документации описывается новый модуль Az для Azure PowerShell. Этот новый модуль создан с нуля на платформе .NET Standard. Использование .NET Standard позволяет Azure PowerShell запускаться в PowerShell 5.1 в Windows, а также PowerShell Core версии  6.x и выше на любой платформе. Модуль Az теперь является предполагаемым способом для работы с Azure с помощью PowerShell.
На AzureRM будут и дальше приходить исправления ошибок, но новые функции не будут доступны.

В статье [Знакомство с новым модулем Az для Azure PowerShell](new-azureps-module-az.md) узнайте все сведения о новом модуле, включая переименование команд и планы обслуживания AzureRM. Если вы хотите начать работу с использованием нового модуля прямо сейчас, см. раздел [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).

Доступны также [Общие сведения об Azure PowerShell](/powershell/azure/azurerm).

> [!IMPORTANT]
>
> Если общие сведения об Azure PowerShell обновляются с учетом имен командлетов нового модуля, то статьи все еще используют команды AzureRM. После установки модуля Az рекомендуется включить псевдонимы командлетов AzureRM с помощью `Enable-AzureRmAlias`. Дополнительные сведения см. в статье [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).

## <a name="run-or-install"></a>Запуск или установка

Вы можете установить Azure PowerShell поверх PowerShell версии 5.1 и выше в Windows, PowerShell Core версии 6.x и выше — на любой платформе, а также запустить среду в Azure Cloud Shell.

* Чтобы запустить Azure PowerShell в браузере с Azure Cloud Shell, ознакомьтесь со статьей [Краткое руководство по использованию PowerShell в Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
* Чтобы установить Azure PowerShell в своей системе, воспользуйтесь [этими инструкциями](install-az-ps.md).

Сведения о последнем выпуске Azure PowerShell см. в [заметках о выпуске](release-notes-azureps.md).

## <a name="get-started"></a>Начало работы

Ознакомьтесь со статьей [Get started with Azure PowerShell](get-started-azureps.md) (Начало работы с Azure PowerShell), чтобы изучить основы Azure PowerShell. Если вы еще не работали с PowerShell, ознакомьтесь с вводными сведениями об этой среде:

* [Установка PowerShell](/powershell/scripting/install/installing-powershell)
* [Scripting with Windows PowerShell](/powershell/scripting/powershell-scripting) (Написание скриптов с помощью Windows PowerShell)
* [Основы PowerShell. (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Основы PowerShell. Часть 1. Начало работы с PowerShell)
* [Краткий курс по началу работы с PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) на сайте Microsoft Virtual Academy

Приведенные ниже примеры помогут вам разобраться в некоторых вариантах использования Azure:

* [Виртуальные машины Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Виртуальные машины Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Веб-приложения](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [Базы данных SQL](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a>Развитие навыков с помощью Microsoft Learn

- [Автоматизация задач Azure с помощью скриптов в PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Дополнительные интерактивные руководства…](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Другие модули Azure PowerShell

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
