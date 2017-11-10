---
title: "Общие сведения о PowerShell для Azure Stack | Документация Майкрософт"
description: "Обзор установки и настройки модуля PowerShell для Azure Stack"
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 49980b361c580a1a00f07c2002241e71f2c0b654
ms.sourcegitcommit: df44d5d9874b55455ec745f1846e06a4b3266d13
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2017
---
# <a name="azure-stack-powershell"></a>PowerShell для Azure Stack

Azure Stack необходимы следующие два модуля PowerShell:  

1. Совместимый с Azure Stack модуль **AzureRM**, который доступен в комплекте установки профиля API версии **2017-03-09-profile**. Командлеты, установленные с помощью этого профиля, могут использовать операторы и пользователи Azure Stack.

2. Последняя версия модуля **AzureStack** — **1.2.11**. Командлеты, установленные с помощью этого модуля, могут использовать только операторы Azure Stack. С помощью командлетов PowerShell, предоставляемых этим модулем, операторы могут выполнять такие задачи, как управление предложениями, планами, службами, квотами и т. д. Чтобы узнать о командлетах PowerShell, доступных в этом модуле, ознакомьтесь со справочными материалами по [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) и [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage).

## <a name="next-steps"></a>Дальнейшие действия

* [Install PowerShell for Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Установка PowerShell для Azure Stack)
* [Configure PowerShell for use with Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Настройка PowerShell для использования с Azure Stack)
