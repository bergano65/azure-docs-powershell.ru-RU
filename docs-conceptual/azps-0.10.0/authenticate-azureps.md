---
title: Вход с помощью Azure PowerShell
description: Сведения о том, как с помощью Azure PowerShell выполнить вход в роли пользователя, субъекта-службы или с помощью управляемых удостоверений для ресурсов Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/04/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 1730d3f8d9fd2783b14c57c94bb3357803623b37
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89242041"
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

> [!IMPORTANT]
>
> Авторизация с учетными данными (на основе имени пользователя и пароля) была отключена в Azure PowerShell из-за изменений в способах авторизации Active Directory и по соображениям безопасности.
> Если вы используете авторизацию с учетными данными, чтобы автоматизировать процесс, [создайте субъект-службу](create-azure-service-principal-azureps.md).

## <a name="sign-in-with-a-service-principal"></a>Вход с использованием субъекта-службы <a name="sp-signin"/>

Субъекты-службы не являются интерактивными учетными записями Azure. Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory. Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.

Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).

Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzAccount`. Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой. Способ входа с использованием субъекта-службы будет зависеть от способа аутентификации: на основе пароля или сертификата.

### <a name="password-based-authentication"></a>Аутентификация на основе пароля

Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Этот командлет отображает запрос на ввод имени пользователя и пароля. Используйте идентификатор субъекта-службы для указанного имени пользователя.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

Если вы используете сценарии автоматизации, вам необходимо создать учетные данные на основе имени пользователя и защищенной строки:

```azurepowershell-interactive
$passwd = ConvertTo-SecureString <use a secure password here> -AsPlainText -Force
$pscredential = New-Object System.Management.Automation.PSCredential('service principal name/id', $passwd)
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

При автоматизации подключений субъекта-службы обязательно придерживайтесь рекомендаций по использованию паролей.

### <a name="certificate-based-authentication"></a>Аутентификация на основе сертификата

Для аутентификации на основе сертификата обязательно, чтобы среда Azure PowerShell могла извлекать данные из локального хранилища сертификатов по отпечатку сертификата.

```azurepowershell-interactive
Connect-AzAccount -ApplicationId $appId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

При использовании субъекта-службы вместо зарегистрированного приложения добавьте аргумент `-ServicePrincipal` и предоставьте идентификатор приложения субъекта-службы в качестве значения параметра `-ApplicationId`.

```azurepowershell-interactive
Connect-AzAccount -ServicePrincipal -ApplicationId $servicePrincipalId -Tenant $tenantId -CertificateThumbprint <thumbprint>
```

В PowerShell 5.1 проверять и администрировать хранилище сертификатов можно с помощью модуля [PKI](/powershell/module/pkiclient). В PowerShell версии 6.х и выше это не настолько просто. Приведенные ниже скрипты демонстрируют, как импортировать существующий сертификат в хранилище сертификатов, к которому имеет доступ PowerShell.

#### <a name="import-a-certificate-in-powershell-51"></a>Импорт сертификата в PowerShell 5.1

```azurepowershell-interactive
# Import a PFX
$credentials = Get-Credential -Message "Provide PFX private key password"
Import-PfxCertificate -FilePath <path to certificate> -Password $credentials.Password -CertStoreLocation cert:\CurrentUser\My
```

#### <a name="import-a-certificate-in-powershell-core-6x-and-later"></a>Импорт сертификата в PowerShell версии 6.х и выше

```azurepowershell-interactive
# Import a PFX
$storeName = [System.Security.Cryptography.X509Certificates.StoreName]::My 
$storeLocation = [System.Security.Cryptography.X509Certificates.StoreLocation]::CurrentUser 
$store = [System.Security.Cryptography.X509Certificates.X509Store]::new($storeName, $storeLocation) 
$certPath = <path to certificate>
$credentials = Get-Credential -Message "Provide PFX private key password"
$flag = [System.Security.Cryptography.X509Certificates.X509KeyStorageFlags]::Exportable 
$certificate = [System.Security.Cryptography.X509Certificates.X509Certificate2]::new($certPath, $credentials.Password, $flag) 
$store.Open([System.Security.Cryptography.X509Certificates.OpenFlags]::ReadWrite) 
$store.Add($Certificate) 
$store.Close()
```

## <a name="sign-in-using-a-managed-identity"></a>Вход с использованием управляемого удостоверения

Управляемые удостоверения — это функция Azure Active Directory. Они представляют собой субъекты-службы, назначенные ресурсам в Azure. Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам. Управляемые удостоверения доступны только в ресурсах в облаке Azure.

Эта команда подключается с помощью управляемого удостоверения среды узла. Например, при выполнении в VirtualMachine с назначенным Управляемым удостоверением службы код может обеспечивать вход с помощью назначенного удостоверения.

```azurepowershell-interactive
 Connect-AzAccount -Identity 
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Вход с использованием нестандартного клиента или в качестве поставщика облачных решений (CSP)

Если ваша учетная запись связана с несколькими клиентами, для входа в систему обязательно используйте параметр `-Tenant` при подключении. Этот параметр можно применить с любым методом входа. При входе в систему в качестве значения для этого параметра можно указать идентификатор объекта Azure клиента (идентификатор клиента) или полное доменное имя клиента.

Если вы являетесь [поставщиком облачных решений](https://azure.microsoft.com/offers/ms-azr-0145p/), значением для `-Tenant`**должен** быть идентификатор клиента.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Вход в другое облако

Облачные службы Azure предоставляют среды, которые соответствуют региональным законам об обработке данных.
Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`.
Этот параметр можно применить с любым методом входа. Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Следующая команда позволяет получить список доступных сред:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```
