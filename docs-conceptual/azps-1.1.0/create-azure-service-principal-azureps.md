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
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342198"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Создание субъекта-службы Azure с помощью Azure PowerShell

Если вы планируете управлять приложением или службой с помощью Azure PowerShell, эти решения нужно запустить в субъекте-службе Azure Active Directory (AAD), а не своей учетной записи. В этой статье объясняется, как создать субъект безопасности с помощью Azure PowerShell.

## <a name="what-is-a-service-principal"></a>Что такое субъект-служба?

Субъект-служба Azure — это идентификатор безопасности, который созданные пользователем приложения, службы и средства автоматизации используют для доступа к определенным ресурсам Azure. Субъектам-службам назначаются определенные разрешения, связанные с их задачами, которые обеспечивают лучший контроль безопасности. Это не похоже на обычный идентификатор пользователя, который обычно разрешает вносить любые изменения.

## <a name="verify-your-own-permission-level"></a>Проверка уровня разрешений

Во-первых, у вас должен быть достаточный уровень разрешений в Azure Active Directory и подписке Azure. У вас должно быть право создавать приложения в Active Directory и назначать роли субъекту-службе.

Проверить, есть ли у вас необходимые разрешения, проще всего на портале. Ознакомьтесь с [проверкой наличия необходимых разрешений на портале](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Создание субъекта-службы для приложения

Войдите в учетную запись Azure, чтобы вы могли создать субъект-службу. Вам должен быть доступен один из следующих способов идентификации развернутого приложения:

* Уникальное имя развернутого приложения, например MyDemoWebApp в следующих примерах
* Идентификатор приложения, глобальный уникальный идентификатор, связанный с развернутым приложением, службой или объектом

### <a name="get-information-about-your-application"></a>Получение сведений о приложении

Используйте командлет `Get-AzADApplication`, чтобы получить сведения о приложении.

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

### <a name="create-a-service-principal-for-your-application"></a>Создание субъекта-службы для приложения

Используйте командлет `New-AzADServicePrincipal`, чтобы создать субъект-службу.

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

Отсюда вы можете напрямую использовать свойство `$servicePrincipal.Secret` в качестве аргумента для `Connect-AzAccount` (см. "Вход с использованием субъекта-службы"), либо вы можете преобразовать `SecureString` в текстовую строку:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($servicePrincipal.Secret)
$password = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
[Runtime.InteropServices.Marshal]::ZeroFreeBSTR($BSTR)
```

### <a name="sign-in-using-the-service-principal"></a>Вход с помощью субъекта-службы

Вы можете войти как новый субъект-служба для приложения, используя `appId`, который вы предоставили, и `password`, который был  
создан. Для субъекта-службы также нужно указать идентификатор клиента. Идентификатор клиента отображается, если вы вошли в Azure с помощью личных учетных данных. Чтобы выполнить вход с помощью субъекта-службы, используйте команды:

```azurepowershell-interactive
$cred = New-Object System.Management.Automation.PSCredential ("00c01aaa-1603-49fc-b6df-b78c4e5138b4", $servicePrincipal.Secret)
Connect-AzAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

После успешного входа вы увидите примерно такие выходные данные:

```output
Environment           : AzureCloud
Account               : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
SubscriptionId        :
SubscriptionName      :
CurrentStorageAccount :
```

Поздравляем! Эти учетные данные можно использовать для запуска приложения. Теперь необходимо настроить права субъекта-службы.

## <a name="managing-roles"></a>Управление ролями

> [!NOTE]
> Управление доступом на основе ролей в Azure (RBAC) — это модель для определения ролей пользователя и субъектов-служб и управления этими ролями. Ролям назначаются связанные наборы разрешений, которые определяют ресурсы, доступные субъекту для чтения, доступа, записи или управления. Дополнительные сведения об RBAC и ролях см. в статье [Встроенные роли для управления доступом на основе ролей в Azure](/azure/active-directory/role-based-access-built-in-roles).

В Azure PowerShell доступны следующие командлеты для управления назначением ролей:

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

По умолчанию субъекту-службе назначена роль **участника**. Возможно, это не лучший выбор для обеспечения взаимодействия приложения со службами Azure, учитывая общие разрешения этой роли.
Роль **читателя** имеет больше ограничений и отлично подходит для приложений с доступом только на чтение. Вы можете просмотреть сведения о разрешениях каждой роли или создать пользовательские разрешения на портале Azure.

В этом примере мы назначаем роль **читателя** предыдущему примеру субъекта-службы и удаляем роль **участника**:

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

Вот как просмотреть текущие назначенные роли:

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

Другие командлеты Azure PowerShell для управления ролями:

* [Get-AzRoleDefinition](/powershell/module/az.resources/Get-azRoleDefinition)
* [New-AzRoleDefinition](/powershell/module/az.resources/New-azRoleDefinition)
* [Remove-AzRoleDefinition](/powershell/module/az.resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.resources/Set-azRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Изменение учетных данных субъекта безопасности

Из соображений безопасности рекомендуется регулярно просматривать разрешения и обновлять пароли. Можно также изменять учетные данные безопасности и управлять ими в случае изменения приложений. Например, можно изменить пароль субъекта-службы, создав новый пароль и удалив старый.

### <a name="add-a-new-password-for-the-service-principal"></a>Добавление нового пароля субъекта-службы

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

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Получение списка учетных данных субъекта-службы

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Удаление старого пароля субъекта-службы

```azurepowershell-interactive
Remove-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```output
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Проверка списка учетных данных субъекта-службы

```azurepowershell-interactive
Get-AzADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```output
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-information-about-the-service-principal"></a>Получение сведений о субъекте-службе

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
