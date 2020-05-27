---
title: Использование субъектов-служб Azure с помощью Azure PowerShell
description: В этой статье описывается, как создавать и использовать субъекты-службы с помощью Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 04/23/2019
ms.openlocfilehash: cf88eb5a477139a0ef5b756ca4e768bbce1b33b7
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387145"
---
# <a name="create-an-azure-service-principal-with-azure-powershell"></a>Создание субъекта-службы Azure с помощью Azure PowerShell

Разрешения для автоматизированных средств, которые используют службы Azure, всегда должны быть ограничены. В качестве замены входу в приложения с использованием учетной записи пользователя с полными правами Azure предлагает субъекты-службы.

Субъект-служба Azure — это удостоверение, созданное для использования с приложениями, размещенными службами и автоматизированными средствами с целью получения доступа к ресурсам Azure. Такой доступ ограничен ролями, которые назначены субъекту-службе, что позволяет управлять разрешениями доступа к ресурсам, в том числе на разных уровнях. По соображениям безопасности мы рекомендуем всегда использовать субъекты-службы с автоматизированными средствами, чтобы не допускать их входа с помощью удостоверения пользователя.

В этой статье описано, как создать субъект-службу, получить сведения о нем и сбросить его с помощью Azure PowerShell.

## <a name="create-a-service-principal"></a>Создание субъекта-службы

Вы можете создать субъект-службу с помощью командлета [New-AzADServicePrincipal](/powershell/module/Az.Resources/New-AzADServicePrincipal). При создании субъекта-службы вы задаете используемый им тип аутентификации для входа.

> [!NOTE]
>
> Если у вашей учетной записи нет прав на создание субъекта-службы, команда `New-AzADServicePrincipal` возвратит сообщение об ошибке, уведомляющее о том, что привилегий недостаточно для выполнения операции. Чтобы получить возможность создавать субъекты-службы, обратитесь к администратору Azure Active Directory.

Субъектам-службам доступно два вида аутентификации: на основе пароля и на основе сертификата.

### <a name="password-based-authentication"></a>Аутентификация на основе пароля

Если другие параметры аутентификации не указаны, используется аутентификация на основе пароля, который генерируется случайным образом. Это рекомендованный метод, если вам нужна аутентификация на основе пароля.

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Возвращаемый объект содержит элемент `Secret`, который является строкой `SecureString` со сгенерированным паролем. Обязательно сохраните это значение в надежном расположении, чтобы выполнять аутентификацию с помощью субъекта-службы. Его значение __не будет__ отображаться в выходных данных консоли. Если вы потеряли пароль, [сбросьте учетные данные субъекта-службы](#reset-credentials).

Следующий код позволяет экспортировать секрет:

```azurepowershell-interactive
$BSTR = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($sp.Secret)
$UnsecureSecret = [System.Runtime.InteropServices.Marshal]::PtrToStringAuto($BSTR)
```

Если вы используете предоставленные пользователями пароли, аргумент `-PasswordCredential` принимает объекты `Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential`. Такие объекты должны иметь допустимые значения `StartDate` и `EndDate`, а также принимать значение `Password` в формате открытого текста. При создании пароля обязательно учитывайте [правила и ограничения для паролей в Azure Active Directory](/azure/active-directory/active-directory-passwords-policy). Не используйте ненадежные пароли или пароли, которые уже используются вами для доступа к другим ресурсам.

```azurepowershell-interactive
Import-Module Az.Resources # Imports the PSADPasswordCredential object
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password=<Choose a strong password>}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

Объект, возвращенный командлетом `New-AzADServicePrincipal`, содержит элементы `Id` и `DisplayName`, каждый из которых можно использовать для входа с помощью субъекта-службы.

> [!IMPORTANT]
>
> Вход с использованием субъекта-службы требует указания идентификатора клиента, для которого был создан субъект-служба. Чтобы получить данные об активном клиенте при создании субъекта-службы, выполните следующую команду __сразу же после__ создания субъекта-службы:
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

### <a name="certificate-based-authentication"></a>Аутентификация на основе сертификата

Субъекты-службы с аутентификацией на основе сертификата создаются с указанием параметра `-CertValue`. Этот параметр принимает строку ASCII открытого сертификата в кодировке Base64 в виде файла PEM, а также файла CRT или CER с текстовой кодировкой. Двоичная кодировка открытых сертификатов не поддерживается. При выполнении этих инструкций предполагается, что у вас уже есть сертификат.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert
```

Вы также можете использовать параметр `-KeyCredential`, который принимает объекты `PSADKeyCredential`. Такие объекты должны иметь допустимые значения `StartDate`, `EndDate`, а их элемент `CertValue` должен иметь значение строки ASCII открытого сертификата в кодировке Base64.

```azurepowershell-interactive
$cert = <public certificate as base64-encoded string>
$credentials = New-Object Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; KeyId=New-Guid; CertValue=$cert}
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -KeyCredential $credentials
```

Объект, возвращенный командлетом `New-AzADServicePrincipal`, содержит элементы `Id` и `DisplayName`, каждый из которых можно использовать для входа с помощью субъекта-службы. Клиентам, которые выполняют вход с использованием субъекта-службы, также нужен доступ к закрытому ключу сертификата.

> [!IMPORTANT]
>
> Вход с использованием субъекта-службы требует указания идентификатора клиента, для которого был создан субъект-служба. Чтобы получить данные об активном клиенте при создании субъекта-службы, выполните следующую команду __сразу же после__ создания субъекта-службы:
>
> ```azurepowershell-interactive
> (Get-AzContext).Tenant.Id
> ```

## <a name="get-an-existing-service-principal"></a>Получение существующего субъекта-службы

Список субъектов-служб для активного клиента можно получить с помощью командлета [Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal). По умолчанию эта команда возвращает __все__ субъекты-службы в клиенте, и в крупных организациях выполнение этой операции может занять много времени. Поэтому мы рекомендуем использовать один из необязательных аргументов фильтрации на стороне сервера:

* `-DisplayNameBeginsWith` — запрашивает субъекты-службы с _префиксом_, который совпадает с указанным значением. Отображаемое имя субъекта-службы представляет собой значение, заданное при создании с помощью параметра `-DisplayName`.
* `-DisplayName`  — запрашивает _точное совпадение_ для имени субъекта-службы.

## <a name="manage-service-principal-roles"></a>Управление ролями субъекта-службы

В Azure PowerShell доступны следующие командлеты для управления назначением ролей:

* [Get-AzRoleAssignment](/powershell/module/az.resources/get-azroleassignment)
* [New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment)
* [Remove-AzRoleAssignment](/powershell/module/az.resources/remove-azroleassignment)

По умолчанию субъекту-службе назначена роль **участника**. Эта роль имеет все разрешения на чтение из учетной записи Azure и запись в нее. Роль **читателя** имеет больше ограничений, предоставляя права доступа только на чтение.  Дополнительные сведения об управлении доступом на основе ролей см. в статье [Встроенные роли для управления доступом на основе ролей в Azure](/azure/active-directory/role-based-access-built-in-roles).

В этом примере мы добавим роль **читателя** и удалим роль **участника**.

```azurepowershell-interactive
New-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Reader"
Remove-AzRoleAssignment -ApplicationId <service principal application ID> -RoleDefinitionName "Contributor"
```

> [!IMPORTANT]
> Командлеты назначения ролей не принимают идентификатор объекта субъекта-службы. Они принимают связанный идентификатор приложения, который генерируется во время создания. Чтобы получить идентификатор приложения для субъекта-службы, воспользуйтесь командлетом `Get-AzADServicePrincipal`.

> [!NOTE]
> Если ваша учетная запись не позволяет назначать роли, вы увидите сообщение об ошибке о том, что ваша учетная запись не авторизована для выполнения действия Microsoft.Authorization/roleAssignments/write. Чтобы получить возможность управлять ролями, обратитесь к администратору Azure Active Directory.

Добавление роли _не_ ограничивает назначенные ранее разрешения. При ограничении разрешений субъекта-службы обязательно удалите роль __участника__.

Чтобы проверить изменения, выведите назначенные роли:

```azurepowershell-interactive
Get-AzRoleAssignment -ServicePrincipalName ServicePrincipalName
```

## <a name="sign-in-using-a-service-principal"></a>Вход с помощью субъекта-службы

Войдите, чтобы протестировать разрешения и учетные данные нового субъекта-службы. Чтобы войти с использованием субъекта-службы, вам нужно указать связанное с ним значение `applicationId` и клиент, для которого он был создан.

Чтобы войти с использованием субъекта-службы с помощью пароля:

```azurepowershell-interactive
# Use the application ID as the username, and the secret as password
$credentials = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $credentials -Tenant <tenant ID> 
```

Для аутентификации на основе сертификата обязательно, чтобы среда Azure PowerShell могла извлекать данные из локального хранилища сертификатов по отпечатку сертификата.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -TenantId $tenantId -CertificateThumbprint <thumbprint>
```

Инструкции по импорту сертификата в хранилище учетных записей, к которому имеет доступ PowerShell, см. в статье [Sign in with Azure PowerShell](authenticate-azureps.md#sp-signin) (Вход с помощью Azure PowerShell).

## <a name="reset-credentials"></a>Сброс учетных данных

Если вы забыли учетные данные для субъекта-службы, воспользуйтесь командлетом [New-AzADSpCredential](/powershell/module/az.resources/new-azadspcredential), чтобы добавить новые учетные данные. Этот командлет принимает те же аргументы и типы учетных данных, что и командлет `New-AzADServicePrincipal`. Если аргументы учетных данных не указаны, создается элемент `PasswordCredential` со случайным паролем.

> [!IMPORTANT]
> Прежде чем назначить новые учетные данные, удалите существующие, чтобы предотвратить вход с их использованием. Для этого выполните командлет [Remove-AzADSpCredential](/powershell/module/az.resources/remove-azadspcredential):
>
> ```azurepowershell-interactive
> Remove-AzADSpCredential -DisplayName ServicePrincipalName
> ```

```azurepowershell-interactive
$newCredential = New-AzADSpCredential -ServicePrincipalName ServicePrincipalName
```
