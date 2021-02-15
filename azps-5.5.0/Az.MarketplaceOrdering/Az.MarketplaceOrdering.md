---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214332"
---
# Az.MarketplaceOrdering Module
## Описание
В разделах этой статьи ются командылеты Azure PowerShell для Azure MarketplaceOrdering в платформе Azure Resource Manager (ARM). Командлеты существуют в области имен Microsoft.Azure.Commands.MarketplaceOrdering. Эти cmdlets позволяют пользователям Azure принимать юридические условия для marketplace, предлагающие дальнейшее программное развертывание для этих решений. Пользователи также могут отклонить набор уже принятых юридических условий.

## Az.MarketplaceOrdering Cmdlets
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Получите условия соглашения для заданного id издателя(Publisher), предложение id(Product) и plan id(Name). Объект терминов, возвращаемый данной командой, передается в Set-AzMarketplaceTerms, чтобы принять юридические условия.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Принятие и отклонение условий для заданного имени издателя (Publisher), предложения id(Product) и плана id(Name). Используйте Get-AzMarketplaceTerms для получения условий соглашения.

