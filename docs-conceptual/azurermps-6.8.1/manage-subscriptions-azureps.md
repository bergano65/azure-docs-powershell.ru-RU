---
title: Управление подписками Azure с помощью Azure PowerShell
description: Управление подписками Azure с помощью Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: e1606ddb02adf1de2cb5496917d61755ac3dad23
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250208"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="2d9a7-103">Управление несколькими подписками Azure</span><span class="sxs-lookup"><span data-stu-id="2d9a7-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="2d9a7-104">Если вы только приступаете к работе с Azure, скорее всего, у вас есть только одна подписка.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-104">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="2d9a7-105">Но если вы уже пользуетесь Azure какое-то время, возможно, вы уже успели создать несколько подписок.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-105">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="2d9a7-106">Вы можете настроить Azure PowerShell для выполнения команд, связанных с определенной подпиской.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-106">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="2d9a7-107">Получите список всех подписок в своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-107">Get a list of all subscriptions in your account.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmSubscription
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

2. <span data-ttu-id="2d9a7-108">Определите подписку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-108">Set the default.</span></span>

    ```azurepowershell-interactive
    Select-AzureRmSubscription -Subscription "My Demos"
    ```

3. <span data-ttu-id="2d9a7-109">Проверьте изменения, выполнив командлет `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-109">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```azurepowershell-interactive
    Get-AzureRmContext
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Demos
    CurrentStorageAccount :
    ```

<span data-ttu-id="2d9a7-110">Когда вы определите подписку по умолчанию, все последующие выполняемые команды Azure PowerShell будут связаны с ней.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-110">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
