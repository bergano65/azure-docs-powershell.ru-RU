---
title: Вход с помощью Azure PowerShell
description: Инструкции по выполнению входа с помощью Azure PowerShell в роли пользователя или субъекта-службы или с помощью MSI.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383980"
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

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a>Вход с использованием управляемого удостоверения службы виртуальных машин Azure

Удостоверение управляемой службы (MSI) — это функция Azure Active Directory, доступная в режиме предварительной версии. Вы можете использовать субъект-службу MSI для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам. Удостоверение MSI доступно только на виртуальных машинах в облаке Azure.

Дополнительные сведения о MSI см. в руководстве по [использованию удостоверения управляемой службы виртуальных машин Azure (MSI) для входа и получения маркеров](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="sign-in-to-another-cloud"></a>Вход в другое облако

Облачные службы Azure предоставляют различные среды, которые соответствуют правилам обработки данных, установленным во многих регионах. Если учетная запись Azure находится в облаке, связанном с одним из этих регионов, то при входе необходимо указать среду. Например, если ваша учетная запись находится в облаке Azure China, то для входа необходимо использовать следующую команду:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
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
