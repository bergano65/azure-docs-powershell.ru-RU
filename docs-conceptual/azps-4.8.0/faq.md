---
title: Вопросы и ответы
description: Часто задаваемые вопросы об Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "92002263"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Часто задаваемые вопросы об Azure PowerShell

## <a name="what-is-azure-powershell"></a>Что такое Azure PowerShell?

Azure PowerShell — это набор командлетов для управления ресурсами Azure непосредственно с помощью PowerShell. В декабре 2018 года модуль PowerShell Az стал общедоступным. Теперь это рекомендуемый модуль PowerShell для взаимодействия с Azure. Дополнительные сведения о модуле PowerShell Az см. в статье [Знакомство с новым модулем Az для Azure PowerShell](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Как отключить предупреждения о критических изменениях в Azure PowerShell?

Чтобы отключить предупреждения о критических изменениях в Azure PowerShell, необходимо задать для переменной среды `SuppressAzurePowerShellBreakingChangeWarnings` значение `true`.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
