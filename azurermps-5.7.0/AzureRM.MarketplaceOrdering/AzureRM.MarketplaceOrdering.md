---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: 198de5436453caf633288e23f804085319a30f73
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93555100"
---
# Модуль AzureRM. MarketplaceOrdering
## Nописание
В этом разделе приведены командлеты PowerShell Azure для Azure MarketplaceOrdering в платформе диспетчера ресурсов Azure (ARM). Командлеты существуют в пространстве имен Microsoft. Azure. Commands. MarketplaceOrdering. Эти командлеты позволяют пользователям Azure принимать юридические условия для рынка, предоставляя более удобное программное развертывание для этих решений. Пользователи также могут отклонить набор юридических слов, которые уже были приняты.

## Командлеты AzureRM. MarketplaceOrdering
### [Get-AzureRmMarketplaceTerms](Get-AzureRmMarketplaceTerms.md)
Получите условия соглашения для определенного кода издателя (издателя), идентификатора предложения (продукта) и кода плана (имени). Объект условий, возвращаемый этой командой, должен быть передан в Set-AzureRmMarketplaceTerms, чтобы принимать юридические условия.

### [Set-AzureRmMarketplaceTerms](Set-AzureRmMarketplaceTerms.md)
Принять или отклонить условия для определенного идентификатора издателя (издателя), идентификатора предложения (продукта) и кода плана (имя). Пожалуйста, используй Get-AzureRmMarketplaceTerms, чтобы получить условия соглашения.

