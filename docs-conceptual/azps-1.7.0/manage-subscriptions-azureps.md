---
title: Управление подписками Azure с помощью Azure PowerShell
description: Управление подписками Azure с помощью Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 29d7c84d0ca9ae8d3e4e22f407b007d2d582f8bc
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364198"
---
# <a name="use-multiple-azure-subscriptions"></a>Использование нескольких подписок Azure

Большинство пользователей Azure обычно используют только одну подписку. Но если вы работаете в нескольких организациях или если доступ к определенным ресурсам в вашей организации разделен по группам, у вас может быть несколько подписок Azure. CLI поддерживает выбор подписки как глобально, так и для отдельных команд.

## <a name="tenants-users-and-subscriptions"></a>Клиенты, пользователи и подписки

При определении различий между клиентами, пользователями и подписками в Azure может возникнуть путаница. _Клиент_ — это сущность Azure Active Directory, которая условно представляет всю организацию. Клиент предполагает наличие минимум одной _подписки_ и одного _пользователя_. Пользователь — это человек, который связан только с одним клиентом — организацией, в которой он работает. Пользователи — это учетные записи для входа в Azure, которые используются, чтобы создавать, использовать и администрировать ресурсы.
Пользователь может иметь доступ к нескольким _подпискам_. Подписки — это соглашения с корпорацией Майкрософт на использование облачных служб, в том числе Azure. Каждый ресурс связан с подпиской.

Дополнительные сведения о различиях между клиентами, пользователями и подписками см. в [словаре терминов, связанных с облачной платформой Azure](/azure/azure-glossary-cloud-terminology).  Чтобы узнать, как добавить новую подписку в клиент Azure Active Directory, см. статью [Как добавить подписку Azure в Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).
Сведения о том, как выполнить вход от имени определенного клиента см. в статье [Sign in with Azure PowerShell](/powershell/azure/authenticate-azureps) (Вход с помощью Azure PowerShell).

## <a name="change-the-active-subscription"></a>Изменение активной подписки

Доступ к ресурсам для подписки в Azure PowerShell требует изменения подписки, связанной с вашим текущим сеансом Azure.
Чтобы сделать это, измените активный контекст сеанса (данные о том, для каких клиента, подписки и пользователя необходимо выполнить командлеты).
Чтобы изменить подписки, сначала нужно извлечь объект контекста Azure PowerShell с помощью командлета [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription), а затем изменить текущий контекст с помощью командлета [Set-AzContext](/powershell/module/az.accounts/set-azcontext).

В следующем примере показано, как получить подписку активного клиента и установить ее в качестве активного сеанса.

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Дополнительные сведения о контекстах Azure PowerShell, в том числе о том, как сохранять их и быстро переключаться между ними для удобной работы с несколькими подписками, см. в статье [Persist credentials with Azure PowerShell contexts](context-persistence.md) (Сохранение учетных данных с контекстами Azure PowerShell).
