---
Module Name: Az.Support
Module Guid: 22d73af7-38c2-4bf6-b56f-4dc9db05d97a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.support
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Az.Support.md
ms.openlocfilehash: a662b6b405296b515d1b69c846775e5209a253dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912397"
---
# AZ. Модуль поддержки
## Nописание
В этом разделе приведены командлеты Azure PowerShell для создания билетов на службу поддержки Azure и управления ими в платформе диспетчера ресурсов Azure (ARM). Командлеты существуют в пространстве имен Microsoft. Azure. Commands. support

## Поддержка командлетов AZ.
### [Get-AzSupportService](Get-AzSupportService.md)
Получает текущий список служб Azure, для которых доступна поддержка. У каждой службы Azure есть собственный набор категорий с названием "Классификация проблем". Получение текущего списка классификаций проблем для службы с помощью Get-AzSupportProblemClassification. Для создания нового билета в службу поддержки с помощью New-AzSupportTicket можно использовать идентификатор GUID для классификации проблем и служб.

### [Get-AzSupportProblemClassification](Get-AzSupportProblemClassification.md)
Получает текущий список классификаций проблем для службы Azure. Для создания нового билета в службу поддержки с помощью New-AzSupportTicket можно использовать идентификатор GUID для классификации проблем и служб. 

### [New-AzSupportContactProfileObject](New-AzSupportContactProfileObject.md)
Вспомогательный командлет для создания объекта профиля контакта поддержки. Вы можете использовать этот объект для New-AzSupportTicket командлета.

### [New-AzSupportTicket](New-AzSupportTicket.md)
Создание нового билета службы поддержки Azure. Эта операция моделируется на [странице запроса новой поддержки](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)Azure.

### [Get-AzSupportTicket](Get-AzSupportTicket.md)
Получает список билетов поддержки. Вы можете получить сведения о билете на полную поддержку по имени билета или отфильтровать билеты поддержки по *состоянию* или *аргументы*.

### [Update-AzSupportTicket](Update-AzSupportTicket.md)
Обновите сведения о серьезности билета в службу поддержки, его статус или контактные данные клиента.

### [Get-AzSupportTicketCommunication](Get-AzSupportTicketCommunication.md)
Получает связь с билетом поддержки. Вы также можете отфильтровать билеты поддержки по *аргументы*   или *CommunicationType*. 

### [New-AzSupportTicketCommunication](New-AzSupportTicketCommunication.md)
Добавляет новый клиентский связь с билетом службы поддержки Azure. 



