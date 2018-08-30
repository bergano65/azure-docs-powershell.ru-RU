---
title: Вход с помощью Azure PowerShell
description: Инструкции по выполнению входа с помощью Azure PowerShell в роли пользователя или субъекта-службы или с помощью MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250632"
---
# <a name="sign-in-with-azure-powershell"></a><span data-ttu-id="35673-103">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="35673-103">Sign in with Azure PowerShell</span></span>

<span data-ttu-id="35673-104">Azure PowerShell поддерживает разные методы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="35673-104">Azure PowerShell supports multiple authentication methods.</span></span> <span data-ttu-id="35673-105">Проще всего начать со входа в интерактивном режиме из командной строки.</span><span class="sxs-lookup"><span data-stu-id="35673-105">The simplest way to get started is to sign in interactively at the command line.</span></span>

## <a name="sign-in-interactively"></a><span data-ttu-id="35673-106">Интерактивный вход</span><span class="sxs-lookup"><span data-stu-id="35673-106">Sign in interactively</span></span>

<span data-ttu-id="35673-107">Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).</span><span class="sxs-lookup"><span data-stu-id="35673-107">To sign in interactively, use the [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount) cmdlet.</span></span>

```azurepowershell
Connect-AzureRmAccount
```

<span data-ttu-id="35673-108">При выполнении этого командлета появится диалоговое окно с предложением ввести адрес электронной почты и пароль, связанные с учетной записью Azure.</span><span class="sxs-lookup"><span data-stu-id="35673-108">When run, this cmdlet will bring up a dialog box prompting you for your email address and password associated with your Azure account.</span></span> <span data-ttu-id="35673-109">Когда вы проходите проверку подлинности, эти сведения сохраняются в текущем сеансе PowerShell, диалоговое окно закрывается, и вы получаете доступ ко всем командлетам Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="35673-109">When you authenticate, that information is saved for the current PowerShell session, the dialog is closed, and you have access to all of the Azure PowerShell cmdlets.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35673-110">Начиная с Azure PowerShell 6.3.0, можно использовать одни учетные данные в нескольких сеансах PowerShell, пока вы остаетесь в системе Windows.</span><span class="sxs-lookup"><span data-stu-id="35673-110">As of Azure PowerShell 6.3.0, your credentials are shared among multiple PowerShell sessions as long as you remain signed in to Windows.</span></span> <span data-ttu-id="35673-111">Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="35673-111">For more information, see the article on [Persistent Credentials](context-persistence.md).</span></span>

## <a name="sign-in-with-a-service-principal"></a><span data-ttu-id="35673-112">Вход с использованием субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="35673-112">Sign in with a service principal</span></span>

<span data-ttu-id="35673-113">Субъекты-службы позволяют создавать неинтерактивные учетные записи, которые можно использовать для управления ресурсами.</span><span class="sxs-lookup"><span data-stu-id="35673-113">Service principals provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="35673-114">Субъекты-службы похожи на учетные записи пользователей, к которым можно применять правила, используя Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="35673-114">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span> <span data-ttu-id="35673-115">Предоставляя минимальные разрешения, необходимые для субъекта-службы, вы можете обеспечить безопасность скриптов службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="35673-115">By granting the minimum permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="35673-116">Если необходимо создать субъект-службу для использования с помощью Azure PowerShell, см. [эту статью](create-azure-service-principal-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="35673-116">If you need to create a service principal for use with Azure PowerShell, see [Create an Azure service principal with Azure PowerShell](create-azure-service-principal-azureps.md).</span></span>

<span data-ttu-id="35673-117">Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="35673-117">To sign in with a service principal, use the `-ServicePrincipal` argument with the `Connect-AzureRmAccount` cmdlet.</span></span> <span data-ttu-id="35673-118">Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="35673-118">You will also need the service princpal's application ID, sign-in credentials, and the tenant ID associate with the service principal.</span></span> <span data-ttu-id="35673-119">Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential).</span><span class="sxs-lookup"><span data-stu-id="35673-119">In order to get the service principal's credentials as the appropriate object, use the [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential) cmdlet.</span></span> <span data-ttu-id="35673-120">Этот командлет вызовет диалоговое окно, в котором нужно ввести идентификатор пользователя и пароль субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="35673-120">This cmdlet will display a dialog box to enter the service principal user ID and password into.</span></span>

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a><span data-ttu-id="35673-121">Вход с использованием управляемого удостоверения службы виртуальных машин Azure</span><span class="sxs-lookup"><span data-stu-id="35673-121">Sign in using an Azure VM Managed Service Identity</span></span>

<span data-ttu-id="35673-122">Удостоверение управляемой службы (MSI) — это функция Azure Active Directory, доступная в режиме предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="35673-122">Managed Service Identity (MSI) is a preview feature of Azure Active Directory.</span></span> <span data-ttu-id="35673-123">Вы можете использовать субъект-службу MSI для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="35673-123">You can use an MSI service principal for sign-in, and acquire an app-only access token to access other resources.</span></span> <span data-ttu-id="35673-124">Удостоверение MSI доступно только на виртуальных машинах в облаке Azure.</span><span class="sxs-lookup"><span data-stu-id="35673-124">MSI is only available on virtual machines running in an Azure cloud.</span></span>

<span data-ttu-id="35673-125">Дополнительные сведения о MSI см. в руководстве по [использованию удостоверения управляемой службы виртуальных машин Azure (MSI) для входа и получения маркеров](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span><span class="sxs-lookup"><span data-stu-id="35673-125">For more information about MSI, see [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi).</span></span>

## <a name="sign-in-to-another-cloud"></a><span data-ttu-id="35673-126">Вход в другое облако</span><span class="sxs-lookup"><span data-stu-id="35673-126">Sign in to another Cloud</span></span>

<span data-ttu-id="35673-127">Облачные службы Azure предоставляют различные среды, которые соответствуют правилам обработки данных, установленным во многих регионах.</span><span class="sxs-lookup"><span data-stu-id="35673-127">Azure cloud services provide different environments that adhere to the data-handling regulations of various regions.</span></span> <span data-ttu-id="35673-128">Если учетная запись Azure находится в облаке, связанном с одним из этих регионов, то при входе необходимо указать среду.</span><span class="sxs-lookup"><span data-stu-id="35673-128">If your Azure account is in a cloud associated with one of these regions, you need to specify the environment when you sign in.</span></span> <span data-ttu-id="35673-129">Например, если ваша учетная запись находится в облаке Azure China, то для входа необходимо использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="35673-129">For example, if you account is in the China cloud you sign on using the following command:</span></span>

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

<span data-ttu-id="35673-130">Чтобы получить список доступных сред, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="35673-130">Use the following command to get a list of available environments:</span></span>

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a><span data-ttu-id="35673-131">Узнайте больше об управлении доступом на основе ролей Azure</span><span class="sxs-lookup"><span data-stu-id="35673-131">Learn more about managing Azure role-based access</span></span>

<span data-ttu-id="35673-132">Дополнительные сведения об аутентификации и управлении подписками в Azure см. в статье [Использование назначений ролей для управления доступом к ресурсам в подписке Azure](/azure/active-directory/role-based-access-control-configure).</span><span class="sxs-lookup"><span data-stu-id="35673-132">For more information about authentication and subscription management in Azure, see [Manage Accounts, Subscriptions, and Administrative Roles](/azure/active-directory/role-based-access-control-configure).</span></span>

<span data-ttu-id="35673-133">Командлеты Azure PowerShell для управления ролями:</span><span class="sxs-lookup"><span data-stu-id="35673-133">Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="35673-134">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="35673-134">Get-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [<span data-ttu-id="35673-135">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35673-135">Get-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="35673-136">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="35673-136">New-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [<span data-ttu-id="35673-137">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35673-137">New-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="35673-138">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="35673-138">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [<span data-ttu-id="35673-139">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35673-139">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="35673-140">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="35673-140">Set-AzureRmRoleDefinition</span></span>](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
