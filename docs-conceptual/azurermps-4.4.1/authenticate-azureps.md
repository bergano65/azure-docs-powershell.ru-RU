---
title: Вход с помощью Azure PowerShell
description: Сведения о том, как с помощью Azure PowerShell выполнить вход в роли пользователя, субъекта-службы или с помощью управляемых удостоверений для ресурсов Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: c3131d3516e50123c48b13dc9e04c0b507a63a58
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425437"
---
# <a name="sign-in-with-azure-powershell"></a>Вход с помощью Azure PowerShell

Azure PowerShell поддерживает разные методы проверки подлинности. Проще всего начать со входа в интерактивном режиме из командной строки.

## <a name="sign-in-interactively"></a>Интерактивный вход

Чтобы выполнить вход в интерактивном режиме, используйте командлет [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell
Connect-AzureRmAccount
```

При выполнении этого командлета появится диалоговое окно с предложением ввести адрес электронной почты и пароль, связанные с учетной записью Azure. Когда вы проходите проверку подлинности, эти сведения сохраняются в текущем сеансе PowerShell, диалоговое окно закрывается, и вы получаете доступ ко всем командлетам Azure PowerShell.

> [!IMPORTANT]
> Начиная с Azure PowerShell 6.3.0, можно использовать одни учетные данные в нескольких сеансах PowerShell, пока вы остаетесь в системе Windows. Дополнительные сведения см. в статье [Использование учетных данных пользователя в разных сеансах PowerShell](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Вход с использованием субъекта-службы

Субъекты-службы позволяют создавать неинтерактивные учетные записи, которые можно использовать для управления ресурсами. Субъекты-службы похожи на учетные записи пользователей, к которым можно применять правила, используя Azure Active Directory. Предоставляя минимальные разрешения, необходимые для субъекта-службы, вы можете обеспечить безопасность скриптов службы автоматизации.

Если необходимо создать субъект-службу для использования с помощью Azure PowerShell, см. [эту статью](create-azure-service-principal-azureps.md).

Чтобы выполнить вход с помощью субъекта-службы, используйте аргумент `-ServicePrincipal` с командлетом `Connect-AzureRmAccount`. Также потребуется идентификатор приложения субъекта-службы, учетные данные для входа и сопоставление идентификатора клиента с субъектом-службой. Чтобы получить учетные данные субъекта-службы как соответствующий объект, используйте командлет [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Этот командлет вызовет диалоговое окно, в котором нужно ввести идентификатор пользователя и пароль субъекта-службы.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-managed-identities-for-azure-resources"></a>Вход с использованием управляемых удостоверений для ресурсов Azure

Управляемые удостоверения для ресурсов Azure — это функция Azure Active Directory. Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам. Управляемые удостоверения доступны только на виртуальных машинах в облаке Azure.

Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в руководстве по [использованию управляемых удостоверений для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-to-another-cloud"></a>Вход в другое облако

Облачные службы Azure предоставляют различные среды, которые соответствуют правилам обработки данных, установленным во многих регионах. Если учетная запись Azure находится в облаке, связанном с одним из этих регионов, то при входе необходимо указать среду. Например, если ваша учетная запись находится в облаке Azure China, то для входа необходимо использовать следующую команду:

```azurepowershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Чтобы получить список доступных сред, используйте следующую команду:

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Узнайте больше об управлении доступом на основе ролей Azure

Дополнительные сведения об аутентификации и управлении подписками в Azure см. в статье [Использование назначений ролей для управления доступом к ресурсам в подписке Azure](/azure/active-directory/role-based-access-control-configure).

Командлеты Azure PowerShell для управления ролями:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
