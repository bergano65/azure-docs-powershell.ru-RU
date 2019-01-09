---
title: Общие сведения об Azure PowerShell
description: Общие сведения об установке и начале работы с модулем Az для Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736466"
---
# <a name="overview-of-azure-powershell"></a>Общие сведения об Azure PowerShell

В Azure PowerShell доступен набор командлетов, которые используют модель [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) для управления ресурсами Azure. Azure PowerShell использует .NET Standard, делая его доступным для Windows, macOS и Linux.
Azure PowerShell также доступен на Azure Cloud Shell.

С помощью [Azure Cloud Shell](/azure/cloud-shell/overview) запускайте Azure PowerShell в браузере или [устанавливайте локально](install-az-ps.md). Ознакомьтесь со статьей [Начало работы с Azure PowerShell](get-started-azureps.md), чтобы изучить основы Azure PowerShell и приступить к работе с Azure.

Сведения о последнем выпуске Azure PowerShell см. в [заметках о выпуске](release-notes-azureps.md).

## <a name="about-the-new-az-module"></a>Сведения о новом модуле Az

В этой документации описывается новый модуль Az для Azure PowerShell. Этот новый модуль создан с нуля на платформе .NET Standard. Использование .NET Standard позволяет Azure PowerShell запускаться в PowerShell 5.x на Windows или в PowerShell 6 на любой другой платформе. Модуль Az теперь является предполагаемым способом для работы с Azure с помощью PowerShell.
На AzureRM будут и дальше приходить исправления ошибок, но новые функции не будут доступны.

В статье [Знакомство с новым модулем Az для Azure PowerShell](new-azureps-module-az.md) узнайте все сведения о новом модуле, включая переименование команд и планы обслуживания AzureRM. Если вы хотите начать работу с использованием нового модуля прямо сейчас, см. раздел [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).

Доступны также [Общие сведения об Azure PowerShell](/powershell/azure/azurerm).

> [!IMPORTANT]
>
> Если общие сведения об Azure PowerShell обновляются с учетом имен командлетов нового модуля, то статьи все еще используют команды AzureRM. После установки модуля Az рекомендуется включить псевдонимы командлетов AzureRM с помощью `Enable-AzureRmAlias`. Дополнительные сведения см. в статье [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).

## <a name="common-scenarios"></a>Распространенные сценарии

Приведенные ниже примеры помогут вам понять, как реализовать типичные сценарии с помощью Azure PowerShell:

* [Виртуальные машины Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [Виртуальные машины Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [Веб-приложения](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [Базы данных SQL](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a>Изучение основ PowerShell

Если вы незнакомы с PowerShell, ознакомьтесь с вводными сведениями о PowerShell.

* [Installing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell) (Установка Windows PowerShell)
* [Scripting with Windows PowerShell](/powershell/scripting/powershell-scripting) (Написание скриптов с помощью Windows PowerShell)

Вы также можете посмотреть этот видеоролик: [Основы PowerShell. Часть 1. Начало работы с PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).

Или пройдите [краткий курс по началу работы с PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) на сайте Microsoft Virtual Academy.

## <a name="build-your-skills-with-microsoft-learn"></a>Развитие навыков с помощью Microsoft Learn

- [Автоматизация задач Azure с помощью скриптов в PowerShell](/learn/modules/automate-azure-tasks-with-powershell/)
- [Другие интерактивные руководства](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a>Другие модули Azure PowerShell

* [Azure Active Directory](/powershell/azure/active-directory/)
* [Azure Information Protection](/powershell/azure/aip/)
* [Azure Service Fabric](/powershell/azure/service-fabric/)
* [Azure ElasticDB](/powershell/azure/elasticdbjobs/)
