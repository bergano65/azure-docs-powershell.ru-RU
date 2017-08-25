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
ms.openlocfilehash: 2a03697e0f3e80d63c48f2dc5615f6c99b9ef716
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <a name="azure-stack-powershell"></a>PowerShell для Azure Stack 

Azure Stack необходимы следующие два модуля PowerShell:  

1. Совместимый с Azure Stack модуль **AzureRM**, который доступен в комплекте установки профиля API версии **2017-03-09-profile**. Командлеты, установленные с помощью этого профиля, могут использовать администраторы и клиенты облака Azure Stack. Чтобы узнать о командлетах PowerShell, доступных в этом профиле, ознакомьтесь со справочными материалами по PowerShell для модуля [AzureRM версии 1.2.9](https://docs.microsoft.com/en-us/powershell/azure/overview?view=azurermps-1.2.9).  

2. Модуль **AzureStack** версии **1.2.9**. Командлеты, установленные с помощью этого модуля, могут использовать только администраторы облака Azure Stack. С помощью командлетов PowerShell, предоставляемых этим модулем, администратор может выполнять такие операции, как управление предложениями, планами, службами, квотами и т. д. Чтобы узнать о командлетах PowerShell, доступных в этом модуле, ознакомьтесь со справочными материалами по [AzureStackAdmin](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.9#azurerm.azurestackadmin) и [AzureStackStorage](https://docs.microsoft.com/en-us/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.9#azurerm.azurestackstorage).

## <a name="next-steps"></a>Дальнейшие действия

* [Install PowerShell for Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Установка PowerShell для Azure Stack)
* [Configure PowerShell for use with Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9) (Настройка PowerShell для использования с Azure Stack)


