---
title: Вопросы и ответы
description: Часто задаваемые вопросы об Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715708"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Часто задаваемые вопросы об Azure PowerShell

## <a name="what-is-azure-powershell"></a>Что такое Azure PowerShell?

Azure PowerShell — это набор командлетов для управления ресурсами Azure непосредственно с помощью PowerShell. В декабре 2018 года модуль PowerShell Az стал общедоступным. Теперь это рекомендуемый модуль PowerShell для взаимодействия с Azure. Дополнительные сведения о модуле PowerShell Az см. в статье [Знакомство с новым модулем Az для Azure PowerShell](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Как отключить предупреждения о критических изменениях в Azure PowerShell?

Чтобы отключить предупреждения о критических изменениях в Azure PowerShell, необходимо задать для переменной среды `SuppressAzurePowerShellBreakingChangeWarnings` значение `true`.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
