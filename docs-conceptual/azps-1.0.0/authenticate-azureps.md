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
# <a name="sign-in-with-azure-powershell"></a>Вход с помощью Azure PowerShell

Azure PowerShell поддерживает несколько методов проверки подлинности. Проще всего начать со входа в интерактивном режиме из командной строки.

## <a name="sign-in-interactively"></a>Интерактивный вход

Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

При запуске этот командлет представит строку токена. Чтобы войти, скопируйте эту строку и вставьте ее в https://microsoft.com/devicelogin в браузере. После этого сеанс PowerShell будет аутентифицирован для подключения к Azure. Эта операция проверки подлинности актуальна для текущего сеанса PowerShell.

> [!IMPORTANT]
>
> Одни учетные данные можно использовать в нескольких сеансах PowerShell, пока вы остаетесь в системе.
> Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Вход с использованием субъекта-службы

Субъекты-службы не являются интерактивными учетными записями Azure. Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory. Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.

Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).

Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzAccount`. Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой. Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Этот командлет представит запрос на ввод идентификатора пользователя и пароля участника службы.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Вход с использованием Управляемого удостоверения службы Azure

Управляемые удостоверения для ресурсов Azure — это функция Azure Active Directory. Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам. Управляемые удостоверения доступны только на виртуальных машинах в облаке Azure.

Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в руководстве по [использованию управляемых удостоверений для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Вход в качестве поставщика облачных решений

Чтобы войти как [поставщик облачных решений (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), используйте параметр `-TenantId`. Как правило, этот параметр может быть предоставлен как идентификатор клиента или доменное имя. Но для входа в качестве поставщика облачных решений нужно указать **идентификатор клиента**.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Вход в другое облако

Облачные службы Azure предоставляют среды, которые соответствуют региональным правилам обработки данных.
Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`.
Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Следующая команда позволяет получить список доступных сред:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Узнайте больше об управлении доступом на основе ролей Azure

Дополнительные сведения об аутентификации и управлении подписками в Azure см. в статье [Использование назначений ролей для управления доступом к ресурсам в подписке Azure](/azure/active-directory/role-based-access-control-configure).

Командлеты Azure PowerShell для управления ролями:

* [Get-AzRoleAssignment](/powershell/module/az.Resources/Get-azRoleAssignment)
* [Get-AzRoleDefinition](/powershell/module/az.Resources/Get-azRoleDefinition)
* [New-AzRoleAssignment](/powershell/module/az.Resources/New-azRoleAssignment)
* [New-AzRoleDefinition](/powershell/module/az.Resources/New-azRoleDefinition)
* [Remove-AzRoleAssignment](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [Remove-AzRoleDefinition](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.Resources/Set-azRoleDefinition)
