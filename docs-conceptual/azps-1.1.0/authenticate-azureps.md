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
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342203"
---
# <a name="sign-in-with-azure-powershell"></a>Вход с помощью Azure PowerShell

Azure PowerShell поддерживает несколько методов проверки подлинности. Проще всего приступить к работе можно с помощью оболочки [Azure Cloud Shell](/azure/cloud-shell/overview), которая автоматически выполняет вход в вашу учетную запись. Если используется локальная установка, вы можете выполнить вход в интерактивном режиме с помощью браузера. При написании скриптов автоматизации рекомендуется использовать [субъект-службу](create-azure-service-principal-azureps.md) с необходимыми разрешениями. Максимально ограничьте разрешения на вход для своего варианта использования, чтобы обеспечить защиту ресурсов Azure.

Когда вы войдете, команды будут выполняться в вашей подписке по умолчанию. Чтобы изменить активную подписку для сеанса, используйте командлет [Set-AzContext](/powershell/module/az.accounts/set-azcontext). Чтобы изменить подписку по умолчанию, используемую при входе в систему с помощью Azure PowerShell, используйте командлет [Set-AzDefault](/powershell/module/az.accounts/set-azdefault).

> [!IMPORTANT]
>
> Одни учетные данные можно использовать в нескольких сеансах PowerShell, пока вы остаетесь в системе.
> Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="sign-in-interactively"></a>Интерактивный вход

Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

При запуске этот командлет представит строку токена. Чтобы войти, скопируйте эту строку и вставьте ее в https://microsoft.com/devicelogin в браузере. Сеанс PowerShell пройдет аутентификацию для подключения к Azure.

## <a name="sign-in-with-credentials"></a>Вход с использованием учетных данных

Также можно войти в систему, используя объект `PSCredential` с правами для подключения к Azure.
Самый простой способ получить объект учетных данных — использовать командлет [Get-Credential](/powershell/module/Microsoft.PowerShell.Security/Get-Credential). Когда вы запустите командлет, вам будет предложено ввести учетные данные: имя пользователя и пароль.

> [!Note]
> Этот способ не работает с учетными записями Майкрософт или с учетными записями, которые используют двухфакторную проверку подлинности.

```azurepowershell-interactive
$creds = Get-Credential
Connect-AzAccount -Credential $creds
```

## <a name="sign-in-with-a-service-principal"></a>Вход с использованием субъекта-службы

Субъекты-службы не являются интерактивными учетными записями Azure. Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory. Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.

Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).

Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzAccount`. Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой. Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Этот командлет представит запрос на ввод идентификатора пользователя и пароля участника службы.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-a-managed-identity"></a>Вход с использованием управляемого удостоверения 

Управляемые удостоверения — это функция Azure Active Directory. Они представляют собой субъекты-службы, назначенные ресурсам в Azure. Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам. Управляемые удостоверения доступны только в ресурсах в облаке Azure.

Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в статье [Как использовать управляемые удостоверения для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Вход с использованием нестандартного клиента или в качестве поставщика облачных решений (CSP)

Если ваша учетная запись связана с несколькими клиентами, для входа в систему обязательно используйте параметр `-TenantId` при подключении. Этот параметр можно применить с любым методом входа. При входе в систему в качестве значения для этого параметра можно указать идентификатор объекта Azure клиента (идентификатор клиента) или полное доменное имя клиента.

Если вы являетесь [поставщиком облачных решений](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/), значением для `-TenantId` **должен** быть идентификатор клиента.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Вход в другое облако

Облачные службы Azure предоставляют среды, которые соответствуют региональным законам об обработке данных.
Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`.
Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Следующая команда позволяет получить список доступных сред:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```