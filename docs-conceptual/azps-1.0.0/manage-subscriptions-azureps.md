---
title: Управление подписками Azure с помощью Azure PowerShell
description: Управление подписками Azure с помощью Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 41cf9b06f736f22eb3c2a9e2fbe1f047534cc09d
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594891"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="9c2a5-103">Управление несколькими подписками Azure</span><span class="sxs-lookup"><span data-stu-id="9c2a5-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="9c2a5-104">Если вы только приступаете к работе с Azure, скорее всего, у вас есть только одна подписка.</span><span class="sxs-lookup"><span data-stu-id="9c2a5-104">If you're brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="9c2a5-105">Но если вы уже пользуетесь Azure какое-то время, возможно, вы уже успели создать несколько подписок.</span><span class="sxs-lookup"><span data-stu-id="9c2a5-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="9c2a5-106">Вы можете настроить Azure PowerShell для выполнения команд, связанных с определенной подпиской.</span><span class="sxs-lookup"><span data-stu-id="9c2a5-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="9c2a5-107">Получите список всех подписок в своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="9c2a5-107">Get a list of all subscriptions in your account.</span></span>

    ```azurepowershell-interactive
    Get-AzSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My DevTest Subscription
    CurrentStorageAccount :

    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

2. <span data-ttu-id="9c2a5-108">Определите подписку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9c2a5-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="9c2a5-109">Проверьте изменения, выполнив командлет `Get-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="9c2a5-109">Verify the change by running the `Get-AzContext` cmdlet.</span></span>

    ```azurepowershell-interactive
    Get-AzContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="9c2a5-110">Когда вы определите подписку по умолчанию, все выполняемые команды Azure PowerShell будут связаны с ней.</span><span class="sxs-lookup"><span data-stu-id="9c2a5-110">Once you set your default subscription, all Azure PowerShell commands run against this subscription.</span></span>