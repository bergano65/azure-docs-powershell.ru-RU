---
title: Вход с помощью Azure PowerShell
description: Сведения о том, как с помощью Azure PowerShell выполнить вход в роли пользователя, субъекта-службы или с помощью управляемых удостоверений для ресурсов Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 7/7/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 8f18af8ed67ecf2aefd353208c07bf812df732d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "92754071"
---
# <a name="sign-in-with-azure-powershell"></a>Вход с помощью Azure PowerShell

Azure PowerShell поддерживает несколько методов проверки подлинности. Проще всего приступить к работе можно с помощью оболочки [Azure Cloud Shell](/azure/cloud-shell/overview), которая автоматически выполняет вход в вашу учетную запись. Если используется локальная установка, вы можете выполнить вход в интерактивном режиме с помощью браузера. При написании скриптов автоматизации рекомендуется использовать [субъект-службу](create-azure-service-principal-azureps.md) с необходимыми разрешениями. Максимально ограничьте разрешения на вход для своего варианта использования, чтобы обеспечить защиту ресурсов Azure.

Если у вас есть доступ более чем к одной подписке, вы входите в первую, которую предлагает Azure. Команды выполняются для этой подписки по умолчанию. Чтобы изменить активную подписку для сеанса, используйте командлет [Set-AzContext](/powershell/module/az.accounts/set-azcontext). Чтобы изменить активную подписку и сохранить ее между сеансами в той же системе, используйте командлет [Select-AzContext](/powershell/module/az.accounts/select-azcontext).

> [!IMPORTANT]
> Одни учетные данные можно использовать в нескольких сеансах PowerShell, пока вы остаетесь в системе.
> Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="sign-in-interactively"></a>Интерактивный вход

Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

При запуске из PowerShell версии 6 и выше этот командлет предоставляет строку токена. Чтобы войти в систему, скопируйте эту строку и вставьте ее в строку [microsoft.com/devicelogin](https://microsoft.com/devicelogin) в веб-браузере. Сеанс PowerShell пройдет аутентификацию для подключения к Azure. Можно указать параметр `UseDeviceAuthentication`, чтобы получить строку токена в Windows PowerShell.

> [!IMPORTANT]
> Авторизация с учетными данными (на основе имени пользователя и пароля) была отключена в Azure PowerShell из-за изменений в способах авторизации Active Directory и по соображениям безопасности. Если вы используете авторизацию с учетными данными, чтобы автоматизировать процесс, [создайте субъект-службу](create-azure-service-principal-azureps.md).

Используйте командлет [Get-AzContext](/powershell/module/az.accounts/get-azcontext), чтобы сохранить идентификатор арендатора в переменной, которая будет использоваться в следующих двух разделах этой статьи.

```azurepowershell-interactive
$tenantId = (Get-AzContext).Tenant.Id
```

## <a name="sign-in-with-a-service-principal"></a>Вход с использованием субъекта-службы <a name="sp-signin"/>

Субъекты-службы не являются интерактивными учетными записями Azure. Как и для других учетных записей пользователей, для управления их разрешениями используется Azure Active Directory. Предоставив субъекту-службе только необходимые разрешения, вы обеспечите защиту скриптов автоматизации.

Сведения о том, как создать субъект-службу для использования с помощью Azure PowerShell, см. в [этой статье](create-azure-service-principal-azureps.md).

Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzAccount`. Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой. Способ входа с использованием субъекта-службы зависит от способа аутентификации: на основе пароля или сертификата.

### <a name="password-based-authentication"></a>Аутентификация на основе пароля

Создайте субъект-службу для использования в примерах в этом разделе. См. статью [Создание субъекта-службы Azure с помощью Azure PowerShell](/powershell/azure/create-azure-service-principal-azureps).

```azurepowershell-interactive
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName
```

Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Этот командлет отображает запрос на ввод имени пользователя и пароля. Используйте значение `applicationID` субъекта-службы в качестве имени пользователя и преобразуйте значение `secret` в обычный текст для пароля.

```azurepowershell-interactive
# Retrieve the plain text password for use with `Get-Credential` in the next command.
$sp.secret | ConvertFrom-SecureString -AsPlainText

$pscredential = Get-Credential -UserName $sp.ApplicationId
Connect-AzAccount -ServicePrincipal -Credential $pscredential -Tenant $tenantId
```

В сценариях автоматизации вам нужно создать учетные данные на основе значений `applicationId` и `secret`субъекта-службы:

```azurepowershell-interactive
$pscredential = New-Object -TypeName System.Management.Automation.PSCredential($sp.ApplicationId, $sp.Secret)
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

В этом примере для подключения используется управляемое удостоверение среды узла. Например, при выполнении в VirtualMachine с назначенным Управляемым удостоверением службы код может обеспечивать вход с помощью назначенного удостоверения.

```azurepowershell-interactive
 Connect-AzAccount -Identity
```

## <a name="sign-in-with-a-non-default-tenant-or-as-a-cloud-solution-provider-csp"></a>Вход с использованием нестандартного клиента или в качестве поставщика облачных решений (CSP)

Если ваша учетная запись связана с несколькими арендаторами, для входа требуется указать параметр `-Tenant` при подключении. Этот параметр работает с любым методом входа. При входе в систему в качестве значения для этого параметра можно указать идентификатор объекта Azure клиента (идентификатор клиента) или полное доменное имя клиента.

Если вы являетесь [поставщиком облачных решений](https://azure.microsoft.com/offers/ms-azr-0145p/), значением для `-Tenant`**должен** быть идентификатор клиента.

```azurepowershell-interactive
Connect-AzAccount -Tenant 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Вход в другое облако

Облачные службы Azure предоставляют среды, которые соответствуют региональным законам об обработке данных. Для учетных записей в региональном облаке нужно при входе указать среду с помощью аргумента `-Environment`. Этот параметр работает с любым методом входа. Например, если ваша учетная запись находится в облаке для Китая, укажите следующее:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Следующая команда позволяет получить список доступных сред:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object -Property Name
```
