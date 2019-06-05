---
title: Использование субъектов-служб Azure с помощью Azure PowerShell
description: В этой статье описывается, как создавать и использовать субъекты-службы с помощью Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: 1980600207cbd65abb8b0bc1afcdc65fbcfd0dc2
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498783"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="e61a8-103">Создание субъекта-службы Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e61a8-103">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="e61a8-104">Разрешения для автоматизированных средств, которые используют службы Azure, всегда должны быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="e61a8-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="e61a8-105">В качестве замены входу в приложения с использованием учетной записи пользователя с полными правами Azure предлагает субъекты-службы.</span><span class="sxs-lookup"><span data-stu-id="e61a8-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span>

<span data-ttu-id="e61a8-106">Субъект-служба Azure — это удостоверение, созданное для использования с приложениями, размещенными службами и автоматизированными средствами с целью получения доступа к ресурсам Azure.</span><span class="sxs-lookup"><span data-stu-id="e61a8-106">An Azure service principal is an identity created for use with applications, hosted services, and automated tools to access Azure resources.</span></span> <span data-ttu-id="e61a8-107">Такой доступ ограничен ролями, которые назначены субъекту-службе, что позволяет управлять разрешениями доступа к ресурсам, в том числе на разных уровнях.</span><span class="sxs-lookup"><span data-stu-id="e61a8-107">This access is restricted by the roles assigned to the service principal, giving you control over which resources can be accessed and at which level.</span></span> <span data-ttu-id="e61a8-108">По соображениям безопасности мы рекомендуем всегда использовать субъекты-службы с автоматизированными средствами, чтобы не допускать их входа с помощью удостоверения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e61a8-108">For security reasons, it's always recommended to use service principals with automated tools rather than allowing them to log in with a user identity.</span></span>

<span data-ttu-id="e61a8-109">В этой статье описано, как создать субъект-службу, получить сведения о нем и сбросить его с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e61a8-109">This article shows you the steps for creating, getting information about, and resetting a service principal with Azure PowerShell.</span></span>

## <a name="create-a-service-principal"></a><span data-ttu-id="e61a8-110">Создание субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="e61a8-110">Create a service principal</span></span>

<span data-ttu-id="e61a8-111">Вы можете создать субъект-службу с помощью командлета [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal).</span><span class="sxs-lookup"><span data-stu-id="e61a8-111">Create a service principal with the [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal) cmdlet.</span></span> <span data-ttu-id="e61a8-112">При создании субъекта-службы вы задаете используемый им тип аутентификации для входа.</span><span class="sxs-lookup"><span data-stu-id="e61a8-112">When creating a service principal, you choose the type of sign-in authentication it uses.</span></span>

> [!NOTE]
>
> <span data-ttu-id="e61a8-113">Если у вашей учетной записи нет прав на создание субъекта-службы, команда `New-AzADServicePrincipal` возвратит сообщение об ошибке, уведомляющее о том, что привилегий недостаточно для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="e61a8-113">If your account doesn't have permission to create a service principal, `New-AzADServicePrincipal` will return an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="e61a8-114">Чтобы получить возможность создавать субъекты-службы, обратитесь к администратору Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e61a8-114">Contact your Azure Active Directory admin to create a service principal.</span></span>

<span data-ttu-id="e61a8-115">Субъектам-службам доступно два вида аутентификации: на основе пароля и на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="e61a8-115">There are two types of authentication available for service principals: Password-based authentication, and certificate-based authentication.</span></span>

### <a name="password-based-authentication"></a><span data-ttu-id="e61a8-116">Аутентификация на основе пароля</span><span class="sxs-lookup"><span data-stu-id="e61a8-116">Password-based authentication</span></span>

<span data-ttu-id="e61a8-117">Если другие параметры аутентификации не указаны, используется аутентификация на основе пароля, который генерируется случайным образом.</span><span class="sxs-lookup"><span data-stu-id="e61a8-117">Without any other authentication parameters, password-based authentication is used and a random password created for you.</span></span> <span data-ttu-id="e61a8-118">Это рекомендованный метод, если вам нужна аутентификация на основе пароля.</span><span class="sxs-lookup"><span data-stu-id="e61a8-118">If you want password-based authentication, this method is recommended.</span></span>

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

<span data-ttu-id="e61a8-119">Возвращаемый объект содержит элемент `Secret`, который является строкой `SecureString` со сгенерированным паролем.</span><span class="sxs-lookup"><span data-stu-id="e61a8-119">The returned object contains the `Secret` member, which is a `SecureString` containing the generated password.</span></span> <span data-ttu-id="e61a8-120">Обязательно сохраните это значение в надежном расположении, чтобы выполнять аутентификацию с помощью субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e61a8-120">Make sure that you store this value somewhere secure to authenticate with the service principal.</span></span> <span data-ttu-id="e61a8-121">Его значение __не будет__ отображаться в выходных данных консоли.</span><span class="sxs-lookup"><span data-stu-id="e61a8-121">Its value __won't__ be displayed in the console output.</span></span> <span data-ttu-id="e61a8-122">Если вы потеряли пароль, [сбросьте учетные данные субъекта-службы](#reset-credentials).</span><span class="sxs-lookup"><span data-stu-id="e61a8-122">If you lose the password, [reset the service principal credentials](#reset-credentials).</span></span> 

<span data-ttu-id="e61a8-123">Если вы используете предоставленные пользователями пароли, аргумент `-PasswordCredential` принимает объекты `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`.</span><span class="sxs-lookup"><span data-stu-id="e61a8-123">For user-supplied passwords, the `-PasswordCredential` argument takes `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential` objects.</span></span> <span data-ttu-id="e61a8-124">Такие объекты должны иметь допустимые значения `StartDate` и `EndDate`, а также принимать значение `Password` в формате открытого текста.</span><span class="sxs-lookup"><span data-stu-id="e61a8-124">These objects must have a valid `StartDate` and `EndDate`, and take a plaintext `Password`.</span></span> <span data-ttu-id="e61a8-125">При создании пароля обязательно учитывайте [правила и ограничения для паролей в Azure Active Directory](/azure/active-directory/active-directory-passwords-policy).</span><span class="sxs-lookup"><span data-stu-id="e61a8-125">When creating a password, make sure you follow the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="e61a8-126">Не используйте ненадежные пароли или пароли, которые уже используются вами для доступа к другим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="e61a8-126">Don't use a weak password or reuse a password.</span></span>

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

<span data-ttu-id="e61a8-127">Объект, возвращенный командлетом `New-AzADServicePrincipal`, содержит элементы `Id` и `DisplayName`, каждый из которых можно использовать для входа с помощью субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e61a8-127">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e61a8-128">Вход с использованием субъекта-службы требует указания идентификатора клиента, для которого был создан субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="e61a8-128">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="e61a8-129">Чтобы получить данные об активном клиенте при создании субъекта-службы, выполните следующую команду __сразу же после__ создания субъекта-службы:</span><span class="sxs-lookup"><span data-stu-id="e61a8-129">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a><span data-ttu-id="e61a8-130">Аутентификация на основе сертификата</span><span class="sxs-lookup"><span data-stu-id="e61a8-130">Certificate-based authentication</span></span>

<span data-ttu-id="e61a8-131">Субъекты-службы с аутентификацией на основе сертификата создаются с указанием параметра `-CertValue`.</span><span class="sxs-lookup"><span data-stu-id="e61a8-131">Service principals using certificate-based authentication are created with the `-CertValue` parameter.</span></span> <span data-ttu-id="e61a8-132">Этот параметр принимает строку ASCII открытого сертификата в кодировке Base64</span><span class="sxs-lookup"><span data-stu-id="e61a8-132">This parameter takes a base64-encoded ASCII string of the public certificate.</span></span> <span data-ttu-id="e61a8-133">в виде файла PEM, а также файла CRT или CER с текстовой кодировкой.</span><span class="sxs-lookup"><span data-stu-id="e61a8-133">This is represented by a PEM file, or a text-encoded CRT or CER.</span></span> <span data-ttu-id="e61a8-134">Двоичная кодировка открытых сертификатов не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e61a8-134">Binary encodings of the public certificate aren't supported.</span></span> <span data-ttu-id="e61a8-135">При выполнении этих инструкций предполагается, что у вас уже есть сертификат.</span><span class="sxs-lookup"><span data-stu-id="e61a8-135">These instructions assume that you already have a certificate available.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

<span data-ttu-id="e61a8-136">Вы также можете использовать параметр `-KeyCredential`, который принимает объекты `PSADKeyCredential`.</span><span class="sxs-lookup"><span data-stu-id="e61a8-136">You can also use the `-KeyCredential` parameter, which takes `PSADKeyCredential` objects.</span></span> <span data-ttu-id="e61a8-137">Такие объекты должны иметь допустимые значения `StartDate`, `EndDate`, а их элемент `CertValue` должен иметь значение строки ASCII открытого сертификата в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="e61a8-137">These objects must have a valid `StartDate`, `EndDate`, and have the `CertValue` member set to a base64-encoded ASCII string of the public certificate.</span></span>

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

<span data-ttu-id="e61a8-138">Объект, возвращенный командлетом `New-AzADServicePrincipal`, содержит элементы `Id` и `DisplayName`, каждый из которых можно использовать для входа с помощью субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e61a8-138">The object returned from `New-AzADServicePrincipal` contains the `Id` and `DisplayName` members, either of which can be used for sign in with the service principal.</span></span> <span data-ttu-id="e61a8-139">Клиентам, которые выполняют вход с использованием субъекта-службы, также нужен доступ к закрытому ключу сертификата.</span><span class="sxs-lookup"><span data-stu-id="e61a8-139">Clients which sign in with the service principal also need access to the certificate's private key.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e61a8-140">Вход с использованием субъекта-службы требует указания идентификатора клиента, для которого был создан субъект-служба.</span><span class="sxs-lookup"><span data-stu-id="e61a8-140">Signing in with a service principal requires the tenant ID which the service principal was created under.</span></span> <span data-ttu-id="e61a8-141">Чтобы получить данные об активном клиенте при создании субъекта-службы, выполните следующую команду __сразу же после__ создания субъекта-службы:</span><span class="sxs-lookup"><span data-stu-id="e61a8-141">To get the active tenant when the service principal was created, run the following command __immediately after__ service principal creation:</span></span>
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a><span data-ttu-id="e61a8-142">Получение существующего субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="e61a8-142">Get an existing service principal</span></span>

<span data-ttu-id="e61a8-143">Список субъектов-служб для активного клиента можно получить с помощью командлета [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span><span class="sxs-lookup"><span data-stu-id="e61a8-143">A list of service principals for the currently active tenant can be retrieved with [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal).</span></span> <span data-ttu-id="e61a8-144">По умолчанию эта команда возвращает __все__ субъекты-службы в клиенте, и в крупных организациях выполнение этой операции может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="e61a8-144">By default this command returns __all__ service principals in a tenant, so for large organizations, it may take a long time to return results.</span></span> <span data-ttu-id="e61a8-145">Поэтому мы рекомендуем использовать один из необязательных аргументов фильтрации на стороне сервера:</span><span class="sxs-lookup"><span data-stu-id="e61a8-145">Instead, using one of the optional server-side filtering arguments is recommended:</span></span>

* <span data-ttu-id="e61a8-146">`-DisplayNameBeginsWith` — запрашивает субъекты-службы с _префиксом_, который совпадает с указанным значением.</span><span class="sxs-lookup"><span data-stu-id="e61a8-146">`-DisplayNameBeginsWith` requests service principals that have a _prefix_ that match the provided value.</span></span> <span data-ttu-id="e61a8-147">Отображаемое имя субъекта-службы представляет собой значение, заданное при создании с помощью параметра `-DisplayName`.</span><span class="sxs-lookup"><span data-stu-id="e61a8-147">The display name of a service principal is the value set with `-DisplayName` during creation.</span></span>
* <span data-ttu-id="e61a8-148">`-DisplayName`  — запрашивает _точное совпадение_ для имени субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e61a8-148">`-DisplayName` requests an _exact match_ of a service principal name.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="e61a8-149">Управление ролями субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="e61a8-149">Manage service principal roles</span></span>

<span data-ttu-id="e61a8-150">В Azure PowerShell доступны следующие командлеты для управления назначением ролей:</span><span class="sxs-lookup"><span data-stu-id="e61a8-150">Azure PowerShell has the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="e61a8-151">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e61a8-151">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="e61a8-152">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e61a8-152">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="e61a8-153">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e61a8-153">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="e61a8-154">По умолчанию субъекту-службе назначена роль **участника**.</span><span class="sxs-lookup"><span data-stu-id="e61a8-154">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="e61a8-155">Эта роль имеет все разрешения на чтение из учетной записи Azure и запись в нее.</span><span class="sxs-lookup"><span data-stu-id="e61a8-155">This role has full permissions to read and write to an Azure account.</span></span> <span data-ttu-id="e61a8-156">Роль **читателя** имеет больше ограничений, предоставляя права доступа только на чтение.</span><span class="sxs-lookup"><span data-stu-id="e61a8-156">The **Reader** role is more restrictive, with read-only access.</span></span>  <span data-ttu-id="e61a8-157">Дополнительные сведения об управлении доступом на основе ролей см. в статье [Встроенные роли для управления доступом на основе ролей в Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="e61a8-157">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="e61a8-158">В этом примере мы добавим роль **читателя** и удалим роль **участника**.</span><span class="sxs-lookup"><span data-stu-id="e61a8-158">This example adds the **Reader** role and removes the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> <span data-ttu-id="e61a8-159">Командлеты назначения ролей не принимают идентификатор объекта субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e61a8-159">Role assignment cmdlets don't take the service principal object ID.</span></span> <span data-ttu-id="e61a8-160">Они принимают связанный идентификатор приложения, который генерируется во время создания.</span><span class="sxs-lookup"><span data-stu-id="e61a8-160">They take the associated application ID, which is generated at creation time.</span></span> <span data-ttu-id="e61a8-161">Чтобы получить идентификатор приложения для субъекта-службы, воспользуйтесь командлетом `Get-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="e61a8-161">To get the application ID for a service principal, use `Get-AzADServicePrincipal`.</span></span>

> [!NOTE]
> <span data-ttu-id="e61a8-162">Если ваша учетная запись не позволяет назначать роли, вы увидите сообщение об ошибке о том, что ваша учетная запись не авторизована для выполнения действия Microsoft.Authorization/roleAssignments/write. Чтобы получить возможность управлять ролями, обратитесь к администратору Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e61a8-162">If your account doesn't have permission to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write'." Contact your Azure Active Directory admin to manage roles.</span></span>

<span data-ttu-id="e61a8-163">Добавление роли _не_ ограничивает назначенные ранее разрешения.</span><span class="sxs-lookup"><span data-stu-id="e61a8-163">Adding a role _doesn't_ restrict previously assigned permissions.</span></span> <span data-ttu-id="e61a8-164">При ограничении разрешений субъекта-службы обязательно удалите роль __участника__.</span><span class="sxs-lookup"><span data-stu-id="e61a8-164">When restricting a service principal's permissions, the __Contributor__ role should be removed.</span></span>

<span data-ttu-id="e61a8-165">Чтобы проверить изменения, выведите назначенные роли:</span><span class="sxs-lookup"><span data-stu-id="e61a8-165">The changes can be verified by listing the assigned roles:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a><span data-ttu-id="e61a8-166">Вход с помощью субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="e61a8-166">Sign in using a service principal</span></span>

<span data-ttu-id="e61a8-167">Войдите, чтобы протестировать разрешения и учетные данные нового субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e61a8-167">Test the new service principal's credentials and permissions by signing in.</span></span> <span data-ttu-id="e61a8-168">Чтобы войти с использованием субъекта-службы, вам нужно указать связанное с ним значение `applicationId` и клиент, для которого он был создан.</span><span class="sxs-lookup"><span data-stu-id="e61a8-168">To sign in with a service principal, you need the `applicationId` value associated with it, and the tenant it was created under.</span></span>

<span data-ttu-id="e61a8-169">Чтобы войти с использованием субъекта-службы с помощью пароля:</span><span class="sxs-lookup"><span data-stu-id="e61a8-169">To sign in with a service principal using a password:</span></span>

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

<span data-ttu-id="e61a8-170">Для аутентификации на основе сертификата обязательно, чтобы среда Azure PowerShell могла извлекать данные из локального хранилища сертификатов по отпечатку сертификата.</span><span class="sxs-lookup"><span data-stu-id="e61a8-170">Certificate-based authentication requires that Azure PowerShell can retrieve information from a local certificate store based on a certificate thumbprint.</span></span>

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

<span data-ttu-id="e61a8-171">Инструкции по импорту сертификата в хранилище учетных записей, к которому имеет доступ PowerShell, см. в статье [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin) (Вход с помощью Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="e61a8-171">For instructions on importing a certificate into a credential store accessible by PowerShell, see [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin)</span></span>

## <a name="reset-credentials"></a><span data-ttu-id="e61a8-172">Сброс учетных данных</span><span class="sxs-lookup"><span data-stu-id="e61a8-172">Reset credentials</span></span>

<span data-ttu-id="e61a8-173">Если вы забыли учетные данные для субъекта-службы, воспользуйтесь командлетом [New-AzADSpCredential](/module/az.resources/new-azadspcredential), чтобы добавить новые учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e61a8-173">If you forget the credentials for a service principal, use [New-AzADSpCredential](/module/az.resources/new-azadspcredential) to add a new credential.</span></span> <span data-ttu-id="e61a8-174">Этот командлет принимает те же аргументы и типы учетных данных, что и командлет `New-AzADServicePrincipal`.</span><span class="sxs-lookup"><span data-stu-id="e61a8-174">This cmdlet takes the same credential arguments and types as `New-AzADServicePrincipal`.</span></span> <span data-ttu-id="e61a8-175">Если аргументы учетных данных не указаны, создается элемент `PasswordCredential` со случайным паролем.</span><span class="sxs-lookup"><span data-stu-id="e61a8-175">Without any credential arguments, a new `PasswordCredential` with a random password is created.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e61a8-176">Прежде чем назначить новые учетные данные, удалите существующие, чтобы предотвратить вход с их использованием.</span><span class="sxs-lookup"><span data-stu-id="e61a8-176">Before assigning any new credentials, you may want to remove existing credentials to prevent sign in with them.</span></span> <span data-ttu-id="e61a8-177">Для этого выполните командлет [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):</span><span class="sxs-lookup"><span data-stu-id="e61a8-177">To do so, use the [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential) cmdlet:</span></span>
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```