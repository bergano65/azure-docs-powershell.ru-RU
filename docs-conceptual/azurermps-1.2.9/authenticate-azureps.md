---
title: Вход с помощью Azure PowerShell
description: Вход с помощью Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: edbf17141cac4ea6e41282c8e1dd07c5b738351c
ms.sourcegitcommit: 80a3da199954d0ab78765715fb49793e89a30f12
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/22/2018
ms.locfileid: "52258287"
---
# <a name="log-in-with-azure-powershell"></a>Вход с помощью Azure PowerShell

Azure PowerShell поддерживает разные способы входа в систему. Проще всего начать со входа в интерактивном режиме из командной строки.

## <a name="interactive-log-in"></a>Интерактивный вход

1. Введите `Login-AzureRmAccount`. Появится диалоговое окно с запросом на ввод учетных данных Azure.

2. Введите электронный адрес и пароль, связанные с вашей учетной записью. Azure выполняет проверку подлинности и сохраняет учетные данные, а затем закрывает окно.

## <a name="log-in-with-a-service-principal"></a>Вход с использованием субъекта-службы

Субъекты-службы позволяют создавать неинтерактивные учетные записи, которые можно использовать для управления ресурсами. Субъекты-службы похожи на учетные записи пользователей, к которым можно применять правила, используя Azure Active Directory. Предоставляя минимальные разрешения, необходимые для субъекта-службы, вы можете обеспечить безопасность скриптов службы автоматизации.

1. Если у вас еще нет субъекта-службы, [создайте](create-azure-service-principal-azureps.md) его.

2. Войдите с помощью субъекта-службы.

    ```powershell-interactive
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    Чтобы получить свой идентификатор клиента, войдите в интерактивном режиме, а затем получите идентификатор из подписки.

    ```powershell-interactive
    Get-AzureRmSubscription
    ```

    ```output
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-managed-identities-for-azure-resources"></a>Вход с использованием управляемых удостоверений для ресурсов Azure

Управляемые удостоверения для ресурсов Azure — это функция Azure Active Directory. Вы можете использовать субъект-службу управляемых удостоверений для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.

Дополнительные сведения об управляемых удостоверениях для ресурсов Azure см. в руководстве по [использованию управляемых удостоверений для ресурсов Azure на виртуальной машине Azure для получения маркера доступа](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="log-in-to-another-cloud"></a>Вход в другое облако

Облачные службы Azure предоставляют различные среды, которые соответствуют правилам обработки данных, установленным во многих государствах. Если учетная запись Azure находится в одном из облаков для государственных организаций, то при входе необходимо указать среду. Например, если ваша учетная запись находится в облаке Azure China, то для входа необходимо использовать следующую команду:

```powershell-interactive
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Чтобы получить список доступных сред, используйте следующую команду:

```powershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

```output
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Узнайте больше об управлении доступом на основе ролей Azure

Дополнительные сведения об аутентификации и управлении подписками в Azure см. в статье [Использование назначений ролей для управления доступом к ресурсам в подписке Azure](/azure/active-directory/role-based-access-control-configure).

Командлеты Azure PowerShell для управления ролями

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
