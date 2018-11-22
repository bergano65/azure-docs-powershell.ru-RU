---
title: Управление подписками Azure с помощью Azure PowerShell | Документация Майкрософт
description: Управление подписками Azure с помощью Azure PowerShell
keywords: Azure PowerShell, подписка
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 12e304f32f585c1af40d20579cd46999e0a12395
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/22/2018
ms.locfileid: "52257964"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="c2d72-104">Управление несколькими подписками Azure</span><span class="sxs-lookup"><span data-stu-id="c2d72-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="c2d72-105">Если вы только приступаете к работе с Azure, скорее всего, у вас есть только одна подписка.</span><span class="sxs-lookup"><span data-stu-id="c2d72-105">If you are brand new to Azure, you probably only have a single subscription.</span></span> <span data-ttu-id="c2d72-106">Но если вы уже пользуетесь Azure какое-то время, возможно, вы уже успели создать несколько подписок.</span><span class="sxs-lookup"><span data-stu-id="c2d72-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span> <span data-ttu-id="c2d72-107">Вы можете настроить Azure PowerShell для выполнения команд, связанных с определенной подпиской.</span><span class="sxs-lookup"><span data-stu-id="c2d72-107">You can configure Azure PowerShell to execute commands against a particular subscription.</span></span>

1. <span data-ttu-id="c2d72-108">Получите список всех подписок в своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c2d72-108">Get a list of all subscriptions in your account.</span></span>

    ```powershell-interactive
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

2. <span data-ttu-id="c2d72-109">Определите подписку по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2d72-109">Set the default.</span></span>

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. <span data-ttu-id="c2d72-110">Проверьте изменения, выполнив командлет `Get-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="c2d72-110">Verify the change by running the `Get-AzureRmContext` cmdlet.</span></span>

    ```powershell-interactive
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

<span data-ttu-id="c2d72-111">Когда вы определите подписку по умолчанию, все последующие выполняемые команды Azure PowerShell будут связаны с ней.</span><span class="sxs-lookup"><span data-stu-id="c2d72-111">Once you set your default subscription, all subsequent Azure PowerShell commands run against this subscription.</span></span>
