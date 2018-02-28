---
title: "Создание субъекта-службы Azure с помощью Azure PowerShell"
description: "Создание субъекта-службы для приложения или службы с помощью Azure PowerShell."
keywords: Azure PowerShell, Azure Active Directory, Azure Active Directory, AD, RBAC
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 6eda2d2a729331b212938aa2681d0188a25b734a
ms.sourcegitcommit: 7e77fe7ecd2112d6b4515517509c5c723e750e27
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2018
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Создание субъекта-службы Azure с помощью Azure PowerShell

Если вы планируете управлять приложением или службой с помощью Azure PowerShell, эти решения нужно запустить в субъекте-службе Azure Active Directory (AAD), а не своей учетной записи. В этой статье объясняется, как создать субъект безопасности с помощью Azure PowerShell.

> [!NOTE]
> Можно также создать субъект-службу на портале Azure. Дополнительные сведения см. в статье [Создание приложения Azure Active Directory и субъекта-службы с доступом к ресурсам с помощью портала](/azure/azure-resource-manager/resource-group-create-service-principal-portal).

## <a name="what-is-a-service-principal"></a>Что такое субъект-служба?

Субъект-служба Azure — это идентификатор безопасности, который созданные пользователем приложения, службы и средства автоматизации используют для доступа к определенным ресурсам Azure. Это что-то вроде удостоверения пользователя (имя пользователя и пароль или сертификат) с определенной ролью и строго контролируемыми разрешениями. Субъект-служба должен выполнять только конкретные задачи, в отличие от удостоверений пользователей. Это решение повышает безопасность, если вы предоставите ему минимальный уровень разрешений для выполнения задач управления.

## <a name="verify-your-own-permission-level"></a>Проверка уровня разрешений

Во-первых, у вас должен быть достаточный уровень разрешений в Azure Active Directory и подписке Azure. В частности, у вас должно быть право создавать приложения в Active Directory и назначать роли субъекту-службе.

Проверить, есть ли у вас соответствующие разрешения, проще всего на портале. Ознакомьтесь с [проверкой наличия необходимых разрешений на портале](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).

## <a name="create-a-service-principal-for-your-app"></a>Создание субъекта-службы для приложения

Войдите в учетную запись Azure, чтобы вы могли создать субъект-службу. Вам должен быть доступен один из следующих способов идентификации развернутого приложения:

* Уникальное имя развернутого приложения, например MyDemoWebApp в следующих примерах.
* Идентификатор приложения, глобальный уникальный идентификатор, связанный с развернутым приложением, службой или объектом.

### <a name="get-information-about-your-application"></a>Получение сведений о приложении

Используйте командлет `Get-AzureRmADApplication`, чтобы получить сведения о приложении.

```powershell
Get-AzureRmADApplication -DisplayNameStartWith MyDemoWebApp
```

```
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

Используйте командлет `New-AzureRmADServicePrincipal`, чтобы создать субъект-службу.

```powershell
Add-Type -Assembly System.Web
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADServicePrincipal -ApplicationId 00c01aaa-1603-49fc-b6df-b78c4e5138b4 -Password $password
```

```
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
MyDemoWebApp                   ServicePrincipal               698138e7-d7b6-4738-a866-b4e3081a69e4
```

### <a name="get-information-about-the-service-principal"></a>Получение сведений о субъекте-службе

```powershell
$svcprincipal = Get-AzureRmADServicePrincipal -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
$svcprincipal | Select-Object *
```

```
ServicePrincipalNames : {http://MyDemoWebApp, 00c01aaa-1603-49fc-b6df-b78c4e5138b4}
ApplicationId         : 00c01aaa-1603-49fc-b6df-b78c4e5138b4
DisplayName           : MyDemoWebApp
Id                    : 698138e7-d7b6-4738-a866-b4e3081a69e4
Type                  : ServicePrincipal
```

### <a name="sign-in-using-the-service-principal"></a>Вход с помощью субъекта-службы

Вы можете войти как новый субъект-служба для приложения, используя предоставленные *идентификатор приложения* и *пароль*. Укажите идентификатор клиента своей учетной записи. Идентификатор клиента отображается при входе в Azure рядом с вашими учетными данными.

```powershell
$cred = Get-Credential -UserName $svcprincipal.ApplicationId -Message "Enter Password"
Login-AzureRmAccount -Credential $cred -ServicePrincipal -TenantId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

Выполните следующую команду в новом сеансе PowerShell. Выполнив вход, вы увидите что-то похожее:

```
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

* [Get-AzureRmRoleAssignment](/powershell/module/azurerm.resources/get-azurermroleassignment)
* [New-AzureRmRoleAssignment](/powershell/module/azurerm.resources/new-azurermroleassignment)
* [Remove-AzureRmRoleAssignment](/powershell/module/azurerm.resources/remove-azurermroleassignment)

По умолчанию субъекту-службе назначена роль **участника**. Возможно, это не лучший выбор для обеспечения взаимодействия приложения со службами Azure, учитывая общие разрешения этой роли.
Роль **читателя** имеет больше ограничений и отлично подходит для приложений с доступом только на чтение. Вы можете просмотреть сведения о разрешениях каждой роли или создать пользовательские разрешения на портале Azure.

В этом примере мы назначаем роль **читателя** предыдущему примеру субъекта-службы и удаляем роль **участника**:

```powershell
New-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Reader
```

```
RoleAssignmentId   : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG/providers/Microsoft.Authorization/roleAssignments/818892f2-d075-46a1-a3a2-3a4e1a12fcd5
Scope              : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myRG
DisplayName        : MyDemoWebApp
SignInName         :
RoleDefinitionName : Reader
RoleDefinitionId   : b24988ac-6180-42a0-ab88-20f7382dd24c
ObjectId           : 698138e7-d7b6-4738-a866-b4e3081a69e4
ObjectType         : ServicePrincipal
```

```powershell
Remove-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4 -RoleDefinitionName Contributor
```

Вот как просмотреть текущие назначенные роли:

```powershell
Get-AzureRmRoleAssignment -ResourceGroupName myRG -ObjectId 698138e7-d7b6-4738-a866-b4e3081a69e4
```

```
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

* [Get-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleDefinition](/powershell/module/azurerm.resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/azurerm.resources/Set-AzureRmRoleDefinition)

## <a name="change-the-credentials-of-the-security-principal"></a>Изменение учетных данных субъекта безопасности

Из соображений безопасности рекомендуется регулярно просматривать разрешения и обновлять пароли. Можно также изменять учетные данные безопасности и управлять ими в случае изменения приложений. Например, можно изменить пароль субъекта-службы, создав новый пароль и удалив старый.

### <a name="add-a-new-password-for-the-service-principal"></a>Добавление нового пароля субъекта-службы

```powershell
$password = [System.Web.Security.Membership]::GeneratePassword(16,3)
New-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -Password $password
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```

### <a name="get-a-list-of-credentials-for-the-service-principal"></a>Получение списка учетных данных субъекта-службы

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
5/5/2016 4:55:27 PM 5/5/2017 4:55:27 PM ca9d4846-4972-4c70-b6f5-a4effa60b9bc Password
```

### <a name="remove-the-old-password-from-the-service-principal"></a>Удаление старого пароля субъекта-службы

```powershell
Remove-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp -KeyId ca9d4846-4972-4c70-b6f5-a4effa60b9bc
```

```
Confirm
Are you sure you want to remove credential with keyId '6f801c3e-6fcd-42b9-be8e-320b17ba1d36' for
service principal objectId '698138e7-d7b6-4738-a866-b4e3081a69e4'.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

### <a name="verify-the-list-of-credentials-for-the-service-principal"></a>Проверка списка учетных данных субъекта-службы

```powershell
Get-AzureRmADSpCredential -ServicePrincipalName http://MyDemoWebApp
```

```
StartDate           EndDate             KeyId                                Type
---------           -------             -----                                ----
3/8/2017 5:58:24 PM 3/8/2018 5:58:24 PM 6f801c3e-6fcd-42b9-be8e-320b17ba1d36 Password
```
