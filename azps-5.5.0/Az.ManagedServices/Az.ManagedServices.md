---
Module Name: Az.ManagedServices
Module Guid: fe0ae00c-c482-4e5f-a837-fbc342fdc7e0
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.managedservices
Help Version: 0.0.2
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Az.ManagedServices.md
ms.openlocfilehash: 4b3d901b606e9ee8127d0ef47ea7847338a69a4c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221561"
---
# Модуль Az.ManagedServices
## Описание
Эта функция используется клиентами управляемых поставщиков услуг. Клиенты могут предоставить MSP возможность управлять своей подпиской или группой ресурсов. Кроме предоставления доступа, клиент также может удалить или просмотреть существующий доступ. Они могут просматривать список клиентов, которые предоставили им доступ к подпискам. В этом процессе участвуют два объекта: определение регистрации, определяющее MSP и определения ролей, предоставленные их пользователям. MSP может определить этот объект с помощью marketplace Managed Services, предлагая назначения Access, которые связывают подписку с определением.

## Az.ManagedServices Cmdlets
### [Get-AzManagedServicesAssignment](Get-AzManagedServicesAssignment.md)
Возвращает определенное назначение или список заданий по регистрации.

### [Get-AzManagedServicesDefinition](Get-AzManagedServicesDefinition.md)
Получает определенное определение или список определений регистрации.

### [New-AzManagedServicesAssignment](New-AzManagedServicesAssignment.md)
Создание или обновление регистрационного задания.

### [New-AzManagedServicesDefinition](New-AzManagedServicesDefinition.md)
Создание или обновление определения регистрации.

### [Remove-AzManagedServicesAssignment](Remove-AzManagedServicesAssignment.md)
Удаление регистрационного назначения.

### [Remove-AzManagedServicesDefinition](Remove-AzManagedServicesDefinition.md)
Удаляет определение регистрации.
