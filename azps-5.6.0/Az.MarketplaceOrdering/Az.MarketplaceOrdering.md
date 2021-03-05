---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: 2720635840051dd85eb613fabb1ac32ba32c6f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991063"
---
# Az.MarketplaceOrdering Module
## Описание
В разделах этой статьи ются командылеты Azure PowerShell для azure MarketplaceOrdering в платформе Azure Resource Manager (ARM). Командлеты существуют в области имен Microsoft.Azure.Commands.MarketplaceOrdering. Эти cmdlets позволяют пользователям Azure принимать юридические условия для marketplace, предлагающие дальнейшее программное развертывание для этих решений. Пользователи также могут отклонить набор уже принятых юридических условий.

## Az.MarketplaceOrdering Cmdlets
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Получите условия соглашения для заданного id издателя(Publisher), предложение id(Product) и plan id(Name). Объект условий, возвращаемый данной командой, передается в Set-AzMarketplaceTerms, чтобы принять юридические условия.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Принятие и отклонение условий для заданного имени издателя (Publisher), предложения id(Product) и плана id(Name). Используйте Get-AzMarketplaceTerms, чтобы получить условия соглашения.

