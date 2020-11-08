---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236418"
---
# AZ. ResourceMover Module
## Nописание
Командлеты Microsoft Azure PowerShell: ResourceMover

## Командлеты AZ. ResourceMover
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Создает или обновляет ресурс перемещения в коллекции Move.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Получает коллекцию Move.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Возвращает ресурс перемещения.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Получает список неразрешенных зависимостей.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Фиксирует набор ресурсов, включенных в текст запроса.
Операция Commit инициируется для moveResources в moveState "CommitPending" или "CommitFailed", после успешного завершения которого moveResource moveState выполняет переход на зафиксированный.
Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Удаляет набор ресурсов, включенных в текст запроса.
Операция отмены вызывается для moveResources в moveState "CommitPending" или "DiscardFailed", после успешного завершения которого moveResource moveState выполняет переход к MovePending.
Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Перемещает набор ресурсов, включенных в текст запроса.
Операция перемещения активируется после того, как moveResources находится в moveState "MovePending" или "MoveFailed", после успешного завершения moveResource moveState выполняет переход к CommitPending.
Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Инициирует подготовку к набору ресурсов, включенных в текст запроса.
Операция подготовки находится на moveResources, которая находится в moveState "PreparePending" или "PrepareFailed", после успешного завершения moveResource moveState выполняет переход к MovePending.
Чтобы помочь пользователю предварительно определить операцию, с помощью которой клиент может вызвать операцию, свойство validateOnly имеет значение true.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Создание или обновление коллекции перемещения.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Удаляет коллекцию Move.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Удаляет ресурс перемещения из коллекции Move.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Вычисляет, обрабатывает и проверяет зависимости moveResources в коллекции Move.

