---
title: Вход с помощью Azure PowerShell
description: Сведения о том, как с помощью Azure PowerShell выполнить вход в роли пользователя, субъекта-службы или с помощью управляемых удостоверений для ресурсов Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 80c59a10666c6e3a01e6c33716fce40094fb14be
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145265"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="8f4a7-103">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8f4a7-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="8f4a7-104">Azure PowerShell поддерживает несколько методов проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-104">Azure PowerShell supports several authentication methods.</span></span> <span data-ttu-id="8f4a7-105">Проще всего приступить к работе можно с помощью оболочки [Azure Cloud Shell](/azure/cloud-shell/overview), которая автоматически выполняет вход в вашу учетную запись.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-105">The easiest way to get started is with [Azure Cloud Shell](/azure/cloud-shell/overview), which automatically logs you in.</span></span> <span data-ttu-id="8f4a7-106">Если используется локальная установка, вы можете выполнить вход в интерактивном режиме с помощью браузера.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-106">With a local install, you can sign in interactively through your browser.</span></span> <span data-ttu-id="8f4a7-107">При написании скриптов автоматизации рекомендуется использовать [субъект-службу](create-azure-service-principal-azureps.md) с необходимыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-107">When writing scripts for automation, the recommended approach is to use a [service principal](create-azure-service-principal-azureps.md) with the necessary permissions.</span></span> <span data-ttu-id="8f4a7-108">Максимально ограничьте разрешения на вход для своего варианта использования, чтобы обеспечить защиту ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-108">When you restrict sign-in permissions as much as possible for your use case, you help keep your Azure resources secure.</span></span>

<span data-ttu-id="8f4a7-109">Когда вы войдете, команды будут выполняться в вашей подписке по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-109">After signing in, commands are run against your default subscription.</span></span> <span data-ttu-id="8f4a7-110">Чтобы изменить активную подписку для сеанса, используйте командлет [Set-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="8f4a7-110">To change your active subscription for a session, use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet.</span></span> <span data-ttu-id="8f4a7-111">Чтобы изменить подписку по умолчанию, используемую при входе в систему с помощью Azure PowerShell, используйте командлет [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span><span class="sxs-lookup"><span data-stu-id="8f4a7-111">To change the default subscription used when logging in with Azure PowerShell, use [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="8f4a7-112">Одни учетные данные можно использовать в нескольких сеансах PowerShell, пока вы остаетесь в системе.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-112">Your credentials are shared among multiple PowerShell sessions as long as you remain signed in.</span></span>
> <span data-ttu-id="8f4a7-113">Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="8f4a7-113">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="8f4a7-114">Интерактивный вход</span><span class="sxs-lookup"><span data-stu-id="8f4a7-114">Sign in interactively</span></span>

<span data-ttu-id="8f4a7-115">Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="8f4a7-115">To sign in interactively, use the [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount) cmdlet.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="8f4a7-116">При запуске этот командлет представит строку токена.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-116">When run, this cmdlet will present a token string.</span></span> <span data-ttu-id="8f4a7-117">Чтобы войти, скопируйте эту строку и вставьте ее в https://microsoft.com/devicelogin в браузере.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-117">To sign in, copy this string and paste it into https://microsoft.com/devicelogin in a browser.</span></span> <span data-ttu-id="8f4a7-118">Сеанс PowerShell пройдет аутентификацию для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-118">Your PowerShell session will be authenticated to connect to Azure.</span></span>

## <a name="sign-in-with-credentials"></a><span data-ttu-id="8f4a7-119">Вход с использованием учетных данных</span><span class="sxs-lookup"><span data-stu-id="8f4a7-119">Sign in with credentials</span></span>

<span data-ttu-id="8f4a7-120">Также можно войти в систему, используя объект `PSCredential` с правами для подключения к Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-120">You can also sign in with a `PSCredential` object authorized to connect to Azure.</span></span>
<span data-ttu-id="8f4a7-121">Самый простой способ получить объект учетных данных — использовать командлет [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential).</span><span class="sxs-lookup"><span data-stu-id="8f4a7-121">The easiest way to get a credential object is with the [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential) cmdlet.</span></span> <span data-ttu-id="8f4a7-122">Когда вы запустите командлет, вам будет предложено ввести учетные данные: имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-122">When run, this cmdlet will prompt you for a username/password credential pair.</span></span>

> [!Note]
> <span data-ttu-id="8f4a7-123">Этот способ не работает с учетными записями Майкрософт или с учетными записями, которые используют двухфакторную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-123">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="8f4a7-124">Вход с использованием субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="8f4a7-124">Sign in with a service principal</span></span>

<span data-ttu-id="8f4a7-125">Субъекты-службы не являются интерактивными учетными записями Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-125">Service principals are non-interactive Azure accounts.</span></span> <span data-ttu-id="8f4a7-126">Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-126">Like other user accounts, their permissions are managed with Azure Active Directory.</span></span> <span data-ttu-id="8f4a7-127">Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-127">By granting a service principal only the permissions it needs, your automation scripts stay secure.</span></span>

<span data-ttu-id="8f4a7-128">Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="8f4a7-128">To learn how to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="8f4a7-129">Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-129">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="8f4a7-130">Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-130">You'll also need the service principal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="8f4a7-131">Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="8f4a7-131">To get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="8f4a7-132">Этот командлет представит запрос на ввод идентификатора пользователя и пароля участника службы.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-132">This cmdlet will present a prompt for the service principal user ID and password.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a><span data-ttu-id="8f4a7-133">Вход с использованием управляемого удостоверения</span><span class="sxs-lookup"><span data-stu-id="8f4a7-133">Sign in using a managed identity</span></span> 

<span data-ttu-id="8f4a7-134">Управляемые удостоверения — это функция Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-134">Managed identities are a feature of Azure Active Directory.</span></span> <span data-ttu-id="8f4a7-135">Они представляют собой субъекты-службы, назначенные ресурсам в Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-135">Managed identities are service principals assigned to resources that run in Azure.</span></span> <span data-ttu-id="8f4a7-136">Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-136">You can use a managed identity service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="8f4a7-137">Управляемые удостоверения доступны только в ресурсах в облаке Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-137">Managed identities are only available on resources running in an Azure cloud.</span></span>

<span data-ttu-id="8f4a7-138">Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в статье [Как использовать управляемые удостоверения для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span><span class="sxs-lookup"><span data-stu-id="8f4a7-138">To learn more about managed identities for Azure resources, see [How to use managed identities for Azure resources on an Azure VM to acquire an access token](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).</span></span>

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a><span data-ttu-id="8f4a7-139">Вход с использованием нестандартного клиента или в качестве поставщика облачных решений (CSP)</span><span class="sxs-lookup"><span data-stu-id="8f4a7-139">Sign in with a non-default tenant or as a Cloud Solution Provider (CSP)</span></span>

<span data-ttu-id="8f4a7-140">Если ваша учетная запись связана с несколькими клиентами, для входа в систему обязательно используйте параметр `-TenantId` при подключении.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-140">If your account is associated with more than one tenant, sign-in requires the use of the `-TenantId` parameter when connecting.</span></span> <span data-ttu-id="8f4a7-141">Этот параметр можно применить с любым методом входа.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-141">This parameter will work with any other sign-in method.</span></span> <span data-ttu-id="8f4a7-142">При входе в систему в качестве значения для этого параметра можно указать идентификатор объекта Azure клиента (идентификатор клиента) или полное доменное имя клиента.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-142">When logging in, this parameter value can either be the Azure object ID of the tenant (Tenant ID) or the fully qualified domain name of the tenant.</span></span>

<span data-ttu-id="8f4a7-143">Если вы являетесь [поставщиком облачных решений](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), значением для `-TenantId` **должен** быть идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-143">If you're a [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), the `-TenantId` value **must** be a tenant ID.</span></span>

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="8f4a7-144">Вход в другое облако</span><span class="sxs-lookup"><span data-stu-id="8f4a7-144">Sign in to another Cloud</span></span>

<span data-ttu-id="8f4a7-145">Облачные службы Azure предоставляют среды, которые соответствуют региональным законам об обработке данных.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-145">Azure cloud services offer environments compliant with regional data-handling laws.</span></span>
<span data-ttu-id="8f4a7-146">Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="8f4a7-146">For accounts in a regional cloud, set the environment when you sign in with the `-Environment` argument.</span></span>
<span data-ttu-id="8f4a7-147">Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="8f4a7-147">For example, if your account is in the China cloud:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="8f4a7-148">Следующая команда позволяет получить список доступных сред:</span><span class="sxs-lookup"><span data-stu-id="8f4a7-148">The following command gets a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```