---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: b634b4e547b1e483037cec8efe5772b5460ee1b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242616"
---
# Модуль Az.ResourceMover
## Описание
Microsoft Azure PowerShell: cmdlets ResourceMover

## Az.ResourceMover Cmdlets
### [Add-AzResourceMoverMoveResource](Add-AzResourceMoverMoveResource.md)
Создает или обновляет перемещение ресурса в коллекции перемещения.

### [Get-AzResourceMoverMoveCollection](Get-AzResourceMoverMoveCollection.md)
Возвращает коллекцию перемещения.

### [Get-AzResourceMoverMoveResource](Get-AzResourceMoverMoveResource.md)
Возвращает ресурс перемещения.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Возвращает список разрешенных зависимостей.

### [Invoke-AzResourceMoverCommit](Invoke-AzResourceMoverCommit.md)
Включает в себя набор ресурсов, включенных в запрос.
При успешном завершении перемещениеResources в moveState "CommitPending" или "CommitFailed" запускается для перемещенияResource moveState.
Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.

### [Invoke-AzResourceMoverDiscard](Invoke-AzResourceMoverDiscard.md)
Удаляет набор ресурсов, включенных в тело запроса.
При успешном завершении перемещениеResources в moveState "CommitPending" или "DiscardFailed" запускается операция отклонения moveResourceState.
Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.

### [Invoke-AzResourceMoverInitiateMove](Invoke-AzResourceMoverInitiateMove.md)
Перемещает набор ресурсов, включенных в запрос.
Операция перемещения запускается после перемещенияResources в moveState "MovePending" или "MoveFailed", при успешном завершении перемещениеResource MoveState сделает переход на CommitPending.
Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.

### [Invoke-AzResourceMoverPrepare](Invoke-AzResourceMoverPrepare.md)
Инициирует подготовку к набору ресурсов, включенных в запрос.
Операция подготовки находится на moveResources, которые находятся в moveState 'PreparePending' или 'PrepareFailed', при успешном завершении перемещениеResource MoveState сделает переход на MovePending.
Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.

### [New-AzResourceMoverMoveCollection](New-AzResourceMoverMoveCollection.md)
Создает или обновляет коллекцию перемещения.

### [Remove-AzResourceMoverMoveCollection](Remove-AzResourceMoverMoveCollection.md)
Удаляет коллекцию перемещения.

### [Remove-AzResourceMoverMoveResource](Remove-AzResourceMoverMoveResource.md)
Удаляет ресурс из коллекции перемещения.

### [Resolve-AzResourceMoverMoveCollectionDependency](Resolve-AzResourceMoverMoveCollectionDependency.md)
Вычисляет, устраняет и проверяет зависимости moveResources в коллекции перемещения.

