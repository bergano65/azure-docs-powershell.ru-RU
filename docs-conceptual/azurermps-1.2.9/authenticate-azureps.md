---
title: Вход с помощью Azure PowerShell
description: Вход с помощью Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: edbf17141cac4ea6e41282c8e1dd07c5b738351c
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211610"
---
# <a name="log-in-with-azure-powershell"></a><span data-ttu-id="37e78-103">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="37e78-103">Log in with Azure PowerShell</span></span>

<span data-ttu-id="37e78-104">Azure PowerShell поддерживает разные способы входа в систему.</span><span class="sxs-lookup"><span data-stu-id="37e78-104">Azure PowerShell supports multiple login methods.</span></span> <span data-ttu-id="37e78-105">Проще всего начать со входа в интерактивном режиме из командной строки.</span><span class="sxs-lookup"><span data-stu-id="37e78-105">The simplest way to get started is to log in interactively at the command line.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="37e78-106">Интерактивный вход</span><span class="sxs-lookup"><span data-stu-id="37e78-106">Interactive log in</span></span>

1. <span data-ttu-id="37e78-107">Введите `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="37e78-107">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="37e78-108">Появится диалоговое окно с запросом на ввод учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="37e78-108">You will get dialog box asking for your Azure credentials.</span></span>

2. <span data-ttu-id="37e78-109">Введите электронный адрес и пароль, связанные с вашей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="37e78-109">Type the email address and password associated with your account.</span></span> <span data-ttu-id="37e78-110">Azure выполняет проверку подлинности и сохраняет учетные данные, а затем закрывает окно.</span><span class="sxs-lookup"><span data-stu-id="37e78-110">Azure authenticates and saves the credential information, and then closes the window.</span></span>

## <a name="log-in-with-a-service-principal"></a><span data-ttu-id="37e78-111">Вход с использованием субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="37e78-111">Log in with a service principal</span></span>

<span data-ttu-id="37e78-112">Субъекты-службы позволяют создавать неинтерактивные учетные записи, которые можно использовать для управления ресурсами.</span><span class="sxs-lookup"><span data-stu-id="37e78-112">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="37e78-113">Субъекты-службы похожи на учетные записи пользователей, к которым можно применять правила, используя Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37e78-113">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="37e78-114">Предоставляя минимальные разрешения, необходимые для субъекта-службы, вы можете обеспечить безопасность скриптов службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="37e78-114">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

1. <span data-ttu-id="37e78-115">Если у вас еще нет субъекта-службы, [создайте](create-azure-service-principal-azureps.md) его.</span><span class="sxs-lookup"><span data-stu-id="37e78-115">If you don't already have a service principal, [create one](create-azure-service-principal-azureps.md).</span></span>

2. <span data-ttu-id="37e78-116">Войдите с помощью субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="37e78-116">Log in with the service principal.</span></span>

    ```powershell-interactive
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    <span data-ttu-id="37e78-117">Чтобы получить свой идентификатор клиента, войдите в интерактивном режиме, а затем получите идентификатор из подписки.</span><span class="sxs-lookup"><span data-stu-id="37e78-117">To get your TenantId, log in interactively and then get the TenantId from your subscription.</span></span>

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
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a><span data-ttu-id="37e78-118">Вход с использованием управляемых удостоверений для ресурсов Azure</span><span class="sxs-lookup"><span data-stu-id="37e78-118">Log in using managed identities for Azure resources</span></span>

<span data-ttu-id="37e78-119">Управляемые удостоверения для ресурсов Azure — это функция Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37e78-119">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="37e78-120">Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="37e78-120">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span>

<span data-ttu-id="37e78-121">Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в руководстве по [использованию управляемых удостоверений для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="37e78-121">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="log-in-to-another-cloud"></a><span data-ttu-id="37e78-122">Вход в другое облако</span><span class="sxs-lookup"><span data-stu-id="37e78-122">Log in to another Cloud</span></span>

<span data-ttu-id="37e78-123">Облачные службы Azure предоставляют различные среды, которые соответствуют правилам обработки данных, установленным во многих государствах.</span><span class="sxs-lookup"><span data-stu-id="37e78-123">Azure cloud services provide different environments that adhere to the data-handling regulations of various governments.</span></span> <span data-ttu-id="37e78-124">Если учетная запись Azure находится в одном из облаков для государственных организаций, то при входе необходимо указать среду.</span><span class="sxs-lookup"><span data-stu-id="37e78-124">If your Azure account is in one the government clouds, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="37e78-125">Например, если ваша учетная запись находится в облаке Azure China, то для входа необходимо использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="37e78-125">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```powershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

<span data-ttu-id="37e78-126">Чтобы получить список доступных сред, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="37e78-126">Use the following command to get a list of available environments:</span></span>

```powershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="37e78-127">Узнайте больше об управлении доступом на основе ролей Azure</span><span class="sxs-lookup"><span data-stu-id="37e78-127">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="37e78-128">Дополнительные сведения об аутентификации и управлении подписками в Azure см. в статье [Использование назначений ролей для управления доступом к ресурсам в подписке Azure](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="37e78-128">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="37e78-129">Командлеты Azure PowerShell для управления ролями</span><span class="sxs-lookup"><span data-stu-id="37e78-129">Azure PowerShell cmdlets for role management</span></span>

* [<span data-ttu-id="37e78-130">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37e78-130">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="37e78-131">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="37e78-131">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="37e78-132">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37e78-132">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="37e78-133">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="37e78-133">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="37e78-134">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="37e78-134">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="37e78-135">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="37e78-135">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="37e78-136">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="37e78-136">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
