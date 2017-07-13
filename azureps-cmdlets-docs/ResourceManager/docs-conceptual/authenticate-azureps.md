---
title: "<span data-ttu-id=\"43adc-101\">Вход с помощью Azure PowerShell</span><span class=\"sxs-lookup\"><span data-stu-id=\"43adc-101\">Log in with Azure PowerShell</span></span>"
description: "<span data-ttu-id=\"43adc-102\">Вход с помощью Azure PowerShell</span><span class=\"sxs-lookup\"><span data-stu-id=\"43adc-102\">Log in with Azure PowerShell</span></span>"
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: f6d249ca5bb09c4fe8445ba5b339ffa6012815ed
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="43adc-103">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="43adc-103">Log in with Azure PowerShell</span></span>
<a id="log-in-with-azure-powershell" class="xliff"></a>

<span data-ttu-id="43adc-104">Azure PowerShell поддерживает разные способы входа в систему.</span><span class="sxs-lookup"><span data-stu-id="43adc-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="43adc-105">Проще всего начать со входа в интерактивном режиме из командной строки.</span><span class="sxs-lookup"><span data-stu-id="43adc-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <span data-ttu-id="43adc-106">Интерактивный вход</span><span class="sxs-lookup"><span data-stu-id="43adc-106">Interactive log in</span></span>
<a id="interactive-log-in" class="xliff"></a>

1. <span data-ttu-id="43adc-107">Введите `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="43adc-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="43adc-108">Появится диалоговое окно с запросом на ввод учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="43adc-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="43adc-109">Введите электронный адрес и пароль, связанные с вашей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="43adc-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="43adc-110">Azure выполняет проверку подлинности и сохраняет учетные данные, а затем закрывает окно.</span><span class="sxs-lookup"><span data-stu-id="43adc-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <span data-ttu-id="43adc-111">Вход с использованием субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="43adc-111">Log in with a service principal</span></span>
<a id="log-in-with-a-service-principal" class="xliff"></a>

<span data-ttu-id="43adc-112">Субъекты-службы позволяют создавать неинтерактивные учетные записи, которые можно использовать для управления ресурсами.</span><span class="sxs-lookup"><span data-stu-id="43adc-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="43adc-113">Субъекты-службы похожи на учетные записи пользователей, к которым можно применять правила, используя Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="43adc-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="43adc-114">Предоставляя минимальные разрешения, необходимые для субъекта-службы, вы можете обеспечить безопасность скриптов службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="43adc-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="43adc-115">Если у вас еще нет субъекта-службы, [создайте](create-azure-service-principal-azureps.md) его.</span><span class="sxs-lookup"><span data-stu-id="43adc-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="43adc-116">Войдите с помощью субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="43adc-116">Log in with the service principal.</span></span>

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="43adc-117">Чтобы получить свой идентификатор клиента, войдите в интерактивном режиме, а затем получите идентификатор из подписки.</span><span class="sxs-lookup"><span data-stu-id="43adc-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

## <span data-ttu-id="43adc-118">Вход в другое облако</span><span class="sxs-lookup"><span data-stu-id="43adc-118">Log in to another Cloud</span></span>
<a id="log-in-to-another-cloud" class="xliff"></a>

<span data-ttu-id="43adc-119">Облачные службы Azure предоставляют различные среды, которые соответствуют правилам обработки данных, установленным во многих государствах.</span><span class="sxs-lookup"><span data-stu-id="43adc-119">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="43adc-120">Если учетная запись Azure находится в одном из облаков для государственных организаций, то при входе необходимо указать среду.</span><span class="sxs-lookup"><span data-stu-id="43adc-120">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="43adc-121">Например, если ваша учетная запись находится в облаке Azure China, то для входа необходимо использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="43adc-121">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="43adc-122">Чтобы получить список доступных сред, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="43adc-122">Use the following command to get a list of available environments:</span></span>

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <span data-ttu-id="43adc-123">Узнайте больше об управлении доступом на основе ролей Azure</span><span class="sxs-lookup"><span data-stu-id="43adc-123">Learn more about managing Azure role-based access</span></span>
<a id="learn-more-about-managing-azure-role-based-access" class="xliff"></a>

<span data-ttu-id="43adc-124">Дополнительные сведения об аутентификации и управлении подписками в Azure см. в статье [Использование назначений ролей для управления доступом к ресурсам в подписке Azure](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="43adc-124">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="43adc-125">Командлеты Azure PowerShell для управления ролями</span><span class="sxs-lookup"><span data-stu-id="43adc-125">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="43adc-126">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="43adc-126">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="43adc-127">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="43adc-127">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="43adc-128">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="43adc-128">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="43adc-129">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="43adc-129">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="43adc-130">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="43adc-130">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="43adc-131">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="43adc-131">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="43adc-132">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="43adc-132">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
