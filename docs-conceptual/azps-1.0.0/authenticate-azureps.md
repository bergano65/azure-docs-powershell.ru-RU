---
title: Вход с помощью Azure PowerShell
description: Сведения о том, как с помощью Azure PowerShell выполнить вход в роли пользователя, субъекта-службы или с помощью управляемых удостоверений для ресурсов Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786685"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="5998e-103">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5998e-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="5998e-104">Azure PowerShell поддерживает несколько методов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="5998e-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="5998e-105">Проще всего начать со входа в интерактивном режиме из командной строки.</span><span class="sxs-lookup"><span data-stu-id="5998e-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="5998e-106">Интерактивный вход</span><span class="sxs-lookup"><span data-stu-id="5998e-106">Sign in interactively</span></span>

<span data-ttu-id="5998e-107">Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="5998e-107">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="5998e-108">При запуске этот командлет представит строку токена.</span><span class="sxs-lookup"><span data-stu-id="5998e-108">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="5998e-109">Чтобы войти, скопируйте эту строку и вставьте ее в https://microsoft.com/devicelogin в браузере.</span><span class="sxs-lookup"><span data-stu-id="5998e-109">To log in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="5998e-110">После этого сеанс PowerShell будет аутентифицирован для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="5998e-110">Your PowerShell session will then be authenticated to connect to Azure.</span></span> <span data-ttu-id="5998e-111">Эта операция проверки подлинности актуальна для текущего сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5998e-111">This authentication lasts for the current PowerShell session.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5998e-112">Одни учетные данные можно использовать в нескольких сеансах PowerShell, пока вы остаетесь в системе.</span><span class="sxs-lookup"><span data-stu-id="5998e-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="5998e-113">Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="5998e-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="5998e-114">Вход с использованием субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="5998e-114">Sign in with a service principal</span></span>

<span data-ttu-id="5998e-115">Субъекты-службы не являются интерактивными учетными записями Azure.</span><span class="sxs-lookup"><span data-stu-id="5998e-115">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="5998e-116">Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5998e-116">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="5998e-117">Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5998e-117">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="5998e-118">Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="5998e-118">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="5998e-119">Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="5998e-119">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="5998e-120">Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="5998e-120">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="5998e-121">Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="5998e-121">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="5998e-122">Этот командлет представит запрос на ввод идентификатора пользователя и пароля участника службы.</span><span class="sxs-lookup"><span data-stu-id="5998e-122">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a><span data-ttu-id="5998e-123">Вход с использованием Управляемого удостоверения службы Azure</span><span class="sxs-lookup"><span data-stu-id="5998e-123">Sign in using an Azure Managed Service Identity</span></span>

<span data-ttu-id="5998e-124">Управляемые удостоверения для ресурсов Azure — это функция Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5998e-124">Managed identities for Azure resources is a feature of Azure Active Directory.</span></span> <span data-ttu-id="5998e-125">Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="5998e-125">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="5998e-126">Управляемые удостоверения доступны только на виртуальных машинах в облаке Azure.</span><span class="sxs-lookup"><span data-stu-id="5998e-126">Managed identities are only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="5998e-127">Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в руководстве по [использованию управляемых удостоверений для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="5998e-127">For more information about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="5998e-128">Вход в качестве поставщика облачных решений</span><span class="sxs-lookup"><span data-stu-id="5998e-128">Sign in as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="5998e-129">Чтобы войти как [поставщик облачных решений (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), используйте параметр `-TenantId`.</span><span class="sxs-lookup"><span data-stu-id="5998e-129">A [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) sign-in requires the use of `-TenantId`.</span></span> <span data-ttu-id="5998e-130">Как правило, этот параметр может быть предоставлен как идентификатор клиента или доменное имя.</span><span class="sxs-lookup"><span data-stu-id="5998e-130">Normally, this parameter can be provided as either a tenant ID or a domain name.</span></span> <span data-ttu-id="5998e-131">Но для входа в качестве поставщика облачных решений нужно указать **идентификатор клиента**.</span><span class="sxs-lookup"><span data-stu-id="5998e-131">However, for CSP sign-in, it must be provided a **tenant ID**.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="5998e-132">Вход в другое облако</span><span class="sxs-lookup"><span data-stu-id="5998e-132">Sign in to another Cloud</span></span>

<span data-ttu-id="5998e-133">Облачные службы Azure предоставляют среды, которые соответствуют региональным правилам обработки данных.</span><span class="sxs-lookup"><span data-stu-id="5998e-133">Azure cloud services offer environments compliant with regional data-handling regulations.</span></span>
<span data-ttu-id="5998e-134">Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="5998e-134">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="5998e-135">Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="5998e-135">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="5998e-136">Следующая команда позволяет получить список доступных сред:</span><span class="sxs-lookup"><span data-stu-id="5998e-136">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="5998e-137">Узнайте больше об управлении доступом на основе ролей Azure</span><span class="sxs-lookup"><span data-stu-id="5998e-137">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="5998e-138">Дополнительные сведения об аутентификации и управлении подписками в Azure см. в статье [Использование назначений ролей для управления доступом к ресурсам в подписке Azure](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="5998e-138">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="5998e-139">Командлеты Azure PowerShell для управления ролями:</span><span class="sxs-lookup"><span data-stu-id="5998e-139">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="5998e-140">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5998e-140">Get-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Get-azRoleAssignment)
* [<span data-ttu-id="5998e-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5998e-141">Get-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Get-azRoleDefinition)
* [<span data-ttu-id="5998e-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5998e-142">New-AzRoleAssignment</span></span>](/powershell/module/az.Resources/New-azRoleAssignment)
* [<span data-ttu-id="5998e-143">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5998e-143">New-AzRoleDefinition</span></span>](/powershell/module/az.Resources/New-azRoleDefinition)
* [<span data-ttu-id="5998e-144">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5998e-144">Remove-AzRoleAssignment</span></span>](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [<span data-ttu-id="5998e-145">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5998e-145">Remove-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [<span data-ttu-id="5998e-146">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="5998e-146">Set-AzRoleDefinition</span></span>](/powershell/module/az.Resources/Set-azRoleDefinition)
