---
title: Создание субъекта-службы Azure с помощью Azure PowerShell
description: Создание субъекта-службы для приложения или службы с помощью Azure PowerShell.
keywords: Azure PowerShell, Azure Active Directory, Azure Active Directory, AD, RBAC
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 3e1c5ad280bdb29ce479dd0a478d0ed58237f969
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2018
ms.locfileid: "53594961"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a><span data-ttu-id="aee94-104">Создание субъекта-службы Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aee94-104">Create an Azure service principal with Azure PowerShell</span></span>

<span data-ttu-id="aee94-105">Если вы планируете управлять приложением или службой с помощью Azure PowerShell, эти решения нужно запустить в субъекте-службе Azure Active Directory (AAD), а не своей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="aee94-105">If you plan to manage your app or service with Azure PowerShell, you should run it under an Azure Active Directory (AAD) service principal, rather than your own credentials.</span></span> <span data-ttu-id="aee94-106">В этой статье объясняется, как создать субъект безопасности с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aee94-106">This article steps you through creating a security principal with Azure PowerShell.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="aee94-107">Что такое субъект-служба?</span><span class="sxs-lookup"><span data-stu-id="aee94-107">What is a service principal?</span></span>

<span data-ttu-id="aee94-108">Субъект-служба Azure — это идентификатор безопасности, который созданные пользователем приложения, службы и средства автоматизации используют для доступа к определенным ресурсам Azure.</span><span class="sxs-lookup"><span data-stu-id="aee94-108">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="aee94-109">Субъектам-службам назначаются определенные разрешения, связанные с их задачами, которые обеспечивают лучший контроль безопасности.</span><span class="sxs-lookup"><span data-stu-id="aee94-109">Service principals are assigned specific permissions related to their tasks, giving you better security control.</span></span> <span data-ttu-id="aee94-110">Это не похоже на обычный идентификатор пользователя, который обычно разрешает вносить любые изменения.</span><span class="sxs-lookup"><span data-stu-id="aee94-110">This is unlike a general user identity, which is usually authorized to make any changes.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="aee94-111">Проверка уровня разрешений</span><span class="sxs-lookup"><span data-stu-id="aee94-111">Verify your own permission level</span></span>

<span data-ttu-id="aee94-112">Во-первых, у вас должен быть достаточный уровень разрешений в Azure Active Directory и подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="aee94-112">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="aee94-113">У вас должно быть право создавать приложения в Active Directory и назначать роли субъекту-службе.</span><span class="sxs-lookup"><span data-stu-id="aee94-113">You must be able to create an app in the Active Directory and assign a role to the service principal.</span></span>

<span data-ttu-id="aee94-114">Проверить, есть ли у вас необходимые разрешения, проще всего на портале.</span><span class="sxs-lookup"><span data-stu-id="aee94-114">The easiest way to check whether your account has the right permissions is through the portal.</span></span> <span data-ttu-id="aee94-115">Ознакомьтесь с [проверкой наличия необходимых разрешений на портале](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span><span class="sxs-lookup"><span data-stu-id="aee94-115">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-app"></a><span data-ttu-id="aee94-116">Создание субъекта-службы для приложения</span><span class="sxs-lookup"><span data-stu-id="aee94-116">Create a service principal for your app</span></span>

<span data-ttu-id="aee94-117">Войдите в учетную запись Azure, чтобы вы могли создать субъект-службу.</span><span class="sxs-lookup"><span data-stu-id="aee94-117">Once signed in to your Azure account, you can create the service principal.</span></span> <span data-ttu-id="aee94-118">Вам должен быть доступен один из следующих способов идентификации развернутого приложения:</span><span class="sxs-lookup"><span data-stu-id="aee94-118">You must have one of the following ways to identify your deployed app:</span></span>

* <span data-ttu-id="aee94-119">Уникальное имя развернутого приложения, например MyDemoWebApp в следующих примерах</span><span class="sxs-lookup"><span data-stu-id="aee94-119">The unique name of your deployed app, such as "MyDemoWebApp" in the following examples</span></span>
* <span data-ttu-id="aee94-120">Идентификатор приложения, глобальный уникальный идентификатор, связанный с развернутым приложением, службой или объектом</span><span class="sxs-lookup"><span data-stu-id="aee94-120">The Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="aee94-121">Получение сведений о приложении</span><span class="sxs-lookup"><span data-stu-id="aee94-121">Get information about your application</span></span>

<span data-ttu-id="aee94-122">Используйте командлет `Get-AzADApplication`, чтобы получить сведения о приложении.</span><span class="sxs-lookup"><span data-stu-id="aee94-122">The `Get-AzADApplication` cmdlet can be used to get information about your application.</span></span>

```azurepowershell-interactive
$app = Get-AzADApplication -DisplayNameStartWith MyDemoWebApp
$app
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

### <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="aee94-123">Создание субъекта-службы для приложения</span><span class="sxs-lookup"><span data-stu-id="aee94-123">Create a service principal for your application</span></span>

<span data-ttu-id="aee94-124">Используйте командлет `New-AzADServicePrincipal`, чтобы создать субъект-службу.</span><span class="sxs-lookup"><span data-stu-id="aee94-124">The `New-AzADServicePrincipal` cmdlet is used to create the service principal.</span></span>

```azurepowershell-interactive
$servicePrincipal = New-AzADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4
```

```output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00c01aaa-1603-49fc-b6df-b78c4e5138b4, http://MyDemoWebApp}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
AdfsId                :
Type                  : ServicePrincipal
```

<span data-ttu-id="aee94-125">Отсюда вы можете напрямую использовать свойство `$servicePrincipal.Secret` в качестве аргумента для `Connect-AzAccount` (см. "Вход с использованием субъекта-службы"), либо вы можете преобразовать `SecureString` в текстовую строку:</span><span class="sxs-lookup"><span data-stu-id="aee94-125">From here, you can either directly use the `$servicePrincipal.Secret` property as an argument to `Connect-AzAccount` (see "Sign in using the service principal"), or you can convert this `SecureString` to a plain text string:</span></span>

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="aee94-126">Вход с помощью субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="aee94-126">Sign in using the service principal</span></span>

<span data-ttu-id="aee94-127">Вы можете войти как новый субъект-служба для приложения, используя `appId`, который вы предоставили, и `password`, который был</span><span class="sxs-lookup"><span data-stu-id="aee94-127">You can now sign in as the new service principal for your app using the `appId` you provided and `password` that was</span></span>  
<span data-ttu-id="aee94-128">создан.</span><span class="sxs-lookup"><span data-stu-id="aee94-128">generated.</span></span> <span data-ttu-id="aee94-129">Для субъекта-службы также нужно указать идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="aee94-129">You also need the Tenant ID for the service principal.</span></span> <span data-ttu-id="aee94-130">Идентификатор клиента отображается, если вы вошли в Azure с помощью личных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="aee94-130">Your Tenant ID is displayed when you sign into Azure with your personal credentials.</span></span> <span data-ttu-id="aee94-131">Чтобы выполнить вход с помощью субъекта-службы, используйте команды:</span><span class="sxs-lookup"><span data-stu-id="aee94-131">To sign in with a service principal, use the commands:</span></span>

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="aee94-132">После успешного входа вы увидите примерно такие выходные данные:</span><span class="sxs-lookup"><span data-stu-id="aee94-132">After a successful sign-in you see output like:</span></span>

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

<span data-ttu-id="aee94-133">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="aee94-133">Congratulations!</span></span> <span data-ttu-id="aee94-134">Эти учетные данные можно использовать для запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="aee94-134">You can use these credentials to run your app.</span></span> <span data-ttu-id="aee94-135">Теперь необходимо настроить права субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="aee94-135">Next, you need to adjust the permissions of the service principal.</span></span>

## <a name="managing-roles"></a><span data-ttu-id="aee94-136">Управление ролями</span><span class="sxs-lookup"><span data-stu-id="aee94-136">Managing roles</span></span>

> [!NOTE]
> <span data-ttu-id="aee94-137">Управление доступом на основе ролей в Azure (RBAC) — это модель для определения ролей пользователя и субъектов-служб и управления этими ролями.</span><span class="sxs-lookup"><span data-stu-id="aee94-137">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span> <span data-ttu-id="aee94-138">Ролям назначаются связанные наборы разрешений, которые определяют ресурсы, доступные субъекту для чтения, доступа, записи или управления.</span><span class="sxs-lookup"><span data-stu-id="aee94-138">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span> <span data-ttu-id="aee94-139">Дополнительные сведения об RBAC и ролях см. в статье [Встроенные роли для управления доступом на основе ролей в Azure](/azure/active-directory/role-based-access-built-in-roles).</span><span class="sxs-lookup"><span data-stu-id="aee94-139">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="aee94-140">В Azure PowerShell доступны следующие командлеты для управления назначением ролей:</span><span class="sxs-lookup"><span data-stu-id="aee94-140">Azure PowerShell provides the following cmdlets to manage role assignments:</span></span>

* [<span data-ttu-id="aee94-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="aee94-141">Get-AzRoleAssignment</span></span>](/powershell/module/az.resources/get-azroleassignment)
* [<span data-ttu-id="aee94-142">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="aee94-142">New-AzRoleAssignment</span></span>](/powershell/module/az.resources/new-azroleassignment)
* [<span data-ttu-id="aee94-143">Remove-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="aee94-143">Remove-AzRoleAssignment</span></span>](/powershell/module/az.resources/remove-azroleassignment)

<span data-ttu-id="aee94-144">По умолчанию субъекту-службе назначена роль **участника**.</span><span class="sxs-lookup"><span data-stu-id="aee94-144">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="aee94-145">Возможно, это не лучший выбор для обеспечения взаимодействия приложения со службами Azure, учитывая общие разрешения этой роли.</span><span class="sxs-lookup"><span data-stu-id="aee94-145">It may not be the best choice depending on the scope of your app's interactions with Azure services, given its broad permissions.</span></span>
<span data-ttu-id="aee94-146">Роль **читателя** имеет больше ограничений и отлично подходит для приложений с доступом только на чтение.</span><span class="sxs-lookup"><span data-stu-id="aee94-146">The **Reader** role is more restrictive and can be a good choice for read-only apps.</span></span> <span data-ttu-id="aee94-147">Вы можете просмотреть сведения о разрешениях каждой роли или создать пользовательские разрешения на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="aee94-147">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="aee94-148">В этом примере мы назначаем роль **читателя** предыдущему примеру субъекта-службы и удаляем роль **участника**:</span><span class="sxs-lookup"><span data-stu-id="aee94-148">In this example, we add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurepowershell-interactive
New-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
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
Remove-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

<span data-ttu-id="aee94-149">Вот как просмотреть текущие назначенные роли:</span><span class="sxs-lookup"><span data-stu-id="aee94-149">To view the current roles assigned:</span></span>

```azurepowershell-interactive
Get-AzRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
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

<span data-ttu-id="aee94-150">Другие командлеты Azure PowerShell для управления ролями:</span><span class="sxs-lookup"><span data-stu-id="aee94-150">Other Azure PowerShell cmdlets for role management:</span></span>

* [<span data-ttu-id="aee94-151">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="aee94-151">Get-AzRoleDefinition</span></span>](/powershell/module/az.resources/Get-azRoleDefinition)
* [<span data-ttu-id="aee94-152">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="aee94-152">New-AzRoleDefinition</span></span>](/powershell/module/az.resources/New-azRoleDefinition)
* [<span data-ttu-id="aee94-153">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="aee94-153">Remove-AzRoleDefinition</span></span>](/powershell/module/az.resources/Remove-azRoleDefinition)
* [<span data-ttu-id="aee94-154">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="aee94-154">Set-AzRoleDefinition</span></span>](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a><span data-ttu-id="aee94-155">Изменение учетных данных субъекта безопасности</span><span class="sxs-lookup"><span data-stu-id="aee94-155">Change the credentials of the security principal</span></span>

<span data-ttu-id="aee94-156">Из соображений безопасности рекомендуется регулярно просматривать разрешения и обновлять пароли.</span><span class="sxs-lookup"><span data-stu-id="aee94-156">It's a good security practice to review the permissions and update the password regularly.</span></span> <span data-ttu-id="aee94-157">Можно также изменять учетные данные безопасности и управлять ими в случае изменения приложений.</span><span class="sxs-lookup"><span data-stu-id="aee94-157">You may also want to manage and modify the security credentials as your app changes.</span></span> <span data-ttu-id="aee94-158">Например, можно изменить пароль субъекта-службы, создав новый пароль и удалив старый.</span><span class="sxs-lookup"><span data-stu-id="aee94-158">For example, we can change the password of the service principal by creating a new password and removing the old one.</span></span>

### <a name="add-a-new-password-for-the-service-principal"></a><span data-ttu-id="aee94-159">Добавление нового пароля субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="aee94-159">Add a new password for the service principal</span></span>

```azurepowershell-interactive
New-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
Secret    : System.Security.SecureString
StartDate : 11/16/2018 12:38:23 AM
EndDate   : 11/16/2019 12:38:23 AM
KeyId     : 6f801c3e-6fcd-42b9-be8e-320b17ba1d36
Type      : Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="aee94-160">Получение списка учетных данных субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="aee94-160">Get a list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a><span data-ttu-id="aee94-161">Удаление старого пароля субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="aee94-161">Remove the old password from the service principal</span></span>

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a><span data-ttu-id="aee94-162">Проверка списка учетных данных субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="aee94-162">Verify the list of credentials for the service principal</span></span>

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="aee94-163">Получение сведений о субъекте-службе</span><span class="sxs-lookup"><span data-stu-id="aee94-163">Get information about the service principal</span></span>

```azurepowershell-interactive
$svcprincipal = Get-AzADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```output
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```
