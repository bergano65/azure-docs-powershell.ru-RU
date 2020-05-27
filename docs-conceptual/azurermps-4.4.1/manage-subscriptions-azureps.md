---
title: Управление подписками Azure с помощью Azure PowerShell | Документация Майкрософт
description: Управление подписками Azure с помощью Azure PowerShell
keywords: Azure PowerShell, подписка
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 921da316b1e8a57f0879c87820297de662b2cfd0
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386737"
---
# <a name="manage-multiple-azure-subscriptions"></a>Управление несколькими подписками Azure

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Если вы только приступаете к работе с Azure, скорее всего, у вас есть только одна подписка. Но если вы уже пользуетесь Azure какое-то время, возможно, вы уже успели создать несколько подписок. Вы можете настроить Azure PowerShell для выполнения команд, связанных с определенной подпиской.

1. Получите список всех подписок в своей учетной записи.

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

2. Определите подписку по умолчанию.

    ```powershell-interactive
    Select-AzureRmSubscription -SubscriptionName "My Demos"
    ```

3. Проверьте изменения, выполнив командлет `Get-AzureRmContext`.

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

Когда вы определите подписку по умолчанию, все последующие выполняемые команды Azure PowerShell будут связаны с ней.
