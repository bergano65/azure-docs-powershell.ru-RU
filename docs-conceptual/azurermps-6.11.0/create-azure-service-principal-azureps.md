---
title: Создание субъекта-службы Azure с помощью Azure PowerShell
description: Создание субъекта-службы для приложения или службы с помощью Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active Directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 433a638187f024883c177457e420a759968fed9a
ms.sourcegitcommit: ff44dec6418a449757bded3c6ebe0a7d4c05ee6e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "50738416"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="835f9-104">Создание субъекта-службы Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="835f9-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="835f9-105">Если вы планируете управлять приложением или службой с помощью Azure PowerShell, эти решения нужно запустить в субъекте-службе Azure Active Directory (AAD), а не своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="835f9-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="835f9-106">В этой статье объясняется, как создать субъект безопасности с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="835f9-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

> [!NOTE]
> <span data-ttu-id="835f9-107">Можно также создать субъект-службу на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="835f9-107">You can also create a service principal through the Azure portal.</span></span> <span data-ttu-id="835f9-108">Дополнительные сведения см. в статье [Создание приложения Azure Active Directory и субъекта-службы с доступом к ресурсам с помощью портала](/azure/azure-resource-manager/resource-group-create-service-principal-portal).</span><span class="sxs-lookup"><span data-stu-id="835f9-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="835f9-109">Что такое субъект-служба?</span><span class="sxs-lookup"><span data-stu-id="835f9-109">What is a 'service principal'?</span></span>

<span data-ttu-id="835f9-110">Субъект-служба Azure — это идентификатор безопасности, который созданные пользователем приложения, службы и средства автоматизации используют для доступа к определенным ресурсам Azure.</span><span class="sxs-lookup"><span data-stu-id="835f9-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="835f9-111">Это что-то вроде удостоверения пользователя (имя пользователя и пароль или сертификат) с определенной ролью и строго контролируемыми разрешениями.</span><span class="sxs-lookup"><span data-stu-id="835f9-111">Think of it as a 'user identity' (username and password or certificate) with a specific role, and tightly controlled permissions.</span></span> <span data-ttu-id="835f9-112">В отличие от удостоверений пользователей субъект-служба должен выполнять только определенные задачи.</span><span class="sxs-lookup"><span data-stu-id="835f9-112">A service principal should only need to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="835f9-113">Это решение повышает безопасность, если вы предоставите ему минимальный уровень разрешений для выполнения задач управления.</span><span class="sxs-lookup"><span data-stu-id="835f9-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="835f9-114">Проверка уровня разрешений</span><span class="sxs-lookup"><span data-stu-id="835f9-114">Verify your own permission level</span></span>

<span data-ttu-id="835f9-115">Во-первых, у вас должен быть достаточный уровень разрешений в Azure Active Directory и подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="835f9-115">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="835f9-116">У вас должно быть право создавать приложения в Active Directory и назначать роли субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="835f9-116">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="835f9-117">Проверить, есть ли у вас необходимые разрешения, проще всего на портале.</span><span class="sxs-lookup"><span data-stu-id="835f9-117">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="835f9-118">Ознакомьтесь с [проверкой наличия необходимых разрешений на портале](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="835f9-118">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="835f9-119">Создание субъекта-службы для приложения</span><span class="sxs-lookup"><span data-stu-id="835f9-119">Create a service principal for your app</span></span>

<span data-ttu-id="835f9-120">Войдите в учетную запись Azure, чтобы вы могли создать субъект-службу.</span><span class="sxs-lookup"><span data-stu-id="835f9-120">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="835f9-121">Вам должен быть доступен один из следующих способов идентификации развернутого приложения:</span><span class="sxs-lookup"><span data-stu-id="835f9-121">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="835f9-122">Уникальное имя развернутого приложения, например MyDemoWebApp в следующих примерах.</span><span class="sxs-lookup"><span data-stu-id="835f9-122">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples, or</span></span>
* <span data-ttu-id="835f9-123">Идентификатор приложения, глобальный уникальный идентификатор, связанный с развернутым приложением, службой или объектом.</span><span class="sxs-lookup"><span data-stu-id="835f9-123">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="835f9-124">Получение сведений о приложении</span><span class="sxs-lookup"><span data-stu-id="835f9-124">Get information about your application</span></span>

<span data-ttu-id="835f9-125">Используйте командлет `Get-AzureRmADApplication`, чтобы получить сведения о приложении.</span><span class="sxs-lookup"><span data-stu-id="835f9-125">The `Get-AzureRmADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```output
DisplayName             : MyDemoWebApp
ObjectId                : 775f64cd-0ec8-4b9b-b69a-8b8946022d9f
IdentifierUris          : {http://MyDemoWebApp}
HomePage                : http://www.contoso.com
Type                    : Application
ApplicationId           : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
AvailableToOtherTenants : False
AppPermissions          :
ReplyUrls               : {}
```

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="835f9-126">Создание субъекта-службы для приложения</span><span class="sxs-lookup"><span data-stu-id="835f9-126">Create a service principal for your application</span></span>

<span data-ttu-id="835f9-127">Используйте командлет `New-AzureRmADServicePrincipal`, чтобы создать субъект-службу.</span><span class="sxs-lookup"><span data-stu-id="835f9-127">The `New-AzureRmADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
$securePassword = ConvertTo-SecureString -Force -AsPlainText -String $password
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $securePassword
```

```output
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="835f9-128">Получение сведений о субъекте-службе</span><span class="sxs-lookup"><span data-stu-id="835f9-128">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="835f9-129">Вход с помощью субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="835f9-129">Sign in using the service principal</span></span>

<span data-ttu-id="835f9-130">Вы можете войти как новый субъект-служба для приложения, используя предоставленные *идентификатор приложения* и *пароль*.</span><span class="sxs-lookup"><span data-stu-id="835f9-130">You can now sign in as the new service principal for your app using the *appId* and *password* you provided.</span></span> <span data-ttu-id="835f9-131">Для субъекта-службы также нужно указать идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="835f9-131">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="835f9-132">Идентификатор клиента отображается, если вы вошли в Azure с помощью личных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="835f9-132">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="835f9-133">Чтобы выполнить вход с помощью субъекта-службы, используйте следующие команды:</span><span class="sxs-lookup"><span data-stu-id="835f9-133">To sign in with a service principal, use the following commands:</span></span>

```azurepowershell-interactive
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Connect-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="835f9-134">После успешного входа вы увидите примерно такие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="835f9-134">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="835f9-135">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="835f9-135">Congratulations!</span></span> <span data-ttu-id="835f9-136">Эти учетные данные можно использовать для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="835f9-136">You can use these credentials to run your app.</span></span> <span data-ttu-id="835f9-137">Теперь необходимо настроить права субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="835f9-137">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="835f9-138">Управление ролями</span><span class="sxs-lookup"><span data-stu-id="835f9-138">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="835f9-139">Управление доступом на основе ролей в Azure (RBAC) — это модель для определения ролей пользователя и субъектов-служб и управления этими ролями.</span><span class="sxs-lookup"><span data-stu-id="835f9-139">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="835f9-140">Ролям назначаются связанные наборы разрешений, которые определяют ресурсы, доступные субъекту для чтения, доступа, записи или управления.</span><span class="sxs-lookup"><span data-stu-id="835f9-140">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="835f9-141">Дополнительные сведения об RBAC и ролях см. в статье [Встроенные роли для управления доступом на основе ролей в Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="835f9-141">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="835f9-142">В Azure PowerShell доступны следующие командлеты для управления назначением ролей:</span><span class="sxs-lookup"><span data-stu-id="835f9-142">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="835f9-143">Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="835f9-143">Get-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [<span data-ttu-id="835f9-144">New-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="835f9-144">New-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [<span data-ttu-id="835f9-145">Remove-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="835f9-145">Remove-AzureRmRoleAssignment</span></span>](/powershell/module/azurerm.resources/remove-azurermroleassignment)

<span data-ttu-id="835f9-146">По умолчанию субъекту-службе назначена роль **участника**.</span><span class="sxs-lookup"><span data-stu-id="835f9-146">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="835f9-147">Возможно, это не лучший выбор для обеспечения взаимодействия приложения со службами Azure, учитывая общие разрешения этой роли.</span><span class="sxs-lookup"><span data-stu-id="835f9-147">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="835f9-148">Роль **читателя** имеет больше ограничений и отлично подходит для приложений с доступом только на чтение.</span><span class="sxs-lookup"><span data-stu-id="835f9-148">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="835f9-149">Вы можете просмотреть сведения о разрешениях каждой роли или создать пользовательские разрешения на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="835f9-149">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="835f9-150">В этом примере мы назначаем роль **читателя** предыдущему примеру субъекта-службы и удаляем роль **участника**:</span><span class="sxs-lookup"><span data-stu-id="835f9-150">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```azurepowershell-interactive
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="835f9-151">Вот как просмотреть текущие назначенные роли:</span><span class="sxs-lookup"><span data-stu-id="835f9-151">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```output
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/0906bbd8-9982-4c03-8dae-aeaae8b13f9e
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : acdd72a7-3385-48ef-bd42-f606fba81ae7
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

<span data-ttu-id="835f9-152">Другие командлеты Azure PowerShell для управления ролями:</span><span class="sxs-lookup"><span data-stu-id="835f9-152">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="835f9-153">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="835f9-153">Get-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [<span data-ttu-id="835f9-154">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="835f9-154">New-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [<span data-ttu-id="835f9-155">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="835f9-155">Remove-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [<span data-ttu-id="835f9-156">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="835f9-156">Set-AzureRmRoleDefinition</span></span>](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="835f9-157">Изменение учетных данных субъекта безопасности</span><span class="sxs-lookup"><span data-stu-id="835f9-157">Change the credentials of the security principal</span></span>

<span data-ttu-id="835f9-158">Из соображений безопасности рекомендуется регулярно просматривать разрешения и обновлять пароли.</span><span class="sxs-lookup"><span data-stu-id="835f9-158">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="835f9-159">Можно также изменять учетные данные безопасности и управлять ими в случае изменения приложений.</span><span class="sxs-lookup"><span data-stu-id="835f9-159">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="835f9-160">Например, можно изменить пароль субъекта-службы, создав новый пароль и удалив старый.</span><span class="sxs-lookup"><span data-stu-id="835f9-160">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="835f9-161">Добавление нового пароля субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="835f9-161">Add a new password for the service principal</span></span>

```azurepowershell-interactive
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="835f9-162">Получение списка учетных данных субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="835f9-162">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="835f9-163">Удаление старого пароля субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="835f9-163">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="835f9-164">Проверка списка учетных данных субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="835f9-164">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
