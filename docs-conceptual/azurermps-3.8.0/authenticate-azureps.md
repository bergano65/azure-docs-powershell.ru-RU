---
title: Вход с помощью Azure PowerShell
description: Вход с помощью Azure PowerShell
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 52a2ccba1886c2761d66aee52b27d66e8da4d630
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821536"
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

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    Чтобы получить свой идентификатор клиента, войдите в интерактивном режиме, а затем получите идентификатор из подписки.

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a>Вход с использованием удостоверения управляемой службы виртуальных машин Azure

Удостоверение управляемой службы (MSI) — это функция Azure Active Directory, доступная в режиме предварительной версии. Вы можете использовать субъект-службу MSI для входа и получения маркера доступа только для приложений, обеспечив возможность обращения к другим ресурсам.

Дополнительные сведения о MSI см. в руководстве по [использованию удостоверения управляемой службы виртуальных машин Azure (MSI) для входа и получения маркеров](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="log-in-to-another-cloud"></a>Вход в другое облако

Облачные службы Azure предоставляют различные среды, которые соответствуют правилам обработки данных, установленным во многих государствах. Если учетная запись Azure находится в одном из облаков для государственных организаций, то при входе необходимо указать среду. Например, если ваша учетная запись находится в облаке Azure China, то для входа необходимо использовать следующую команду:

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Чтобы получить список доступных сред, используйте следующую команду:

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
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
