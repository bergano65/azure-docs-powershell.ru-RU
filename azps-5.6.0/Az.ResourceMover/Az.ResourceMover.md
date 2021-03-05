---
Module Name: Az.ResourceMover
Module Guid: 97d87543-8eef-4574-a70d-7317ec4abe54
Download Help Link: https://docs.microsoft.com/powershell/module/az.resourcemover
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Az.ResourceMover.md
ms.openlocfilehash: 0f43535baa284dbe9f7c69aee5a688443172089a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000051"
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

### [Get-AzResourceMoverRequiredForResources](Get-AzResourceMoverRequiredForResources.md)
Список ресурсов для перемещения, для которых требуется ресурс на arm.

### [Get-AzResourceMoverUnresolvedDependency](Get-AzResourceMoverUnresolvedDependency.md)
Возвращает список разрешенных зависимостей.

### [Invoke-AzResourceMoverBulkRemove](Invoke-AzResourceMoverBulkRemove.md)
Удаляет набор ресурсов перемещения, включенных в запрос, из коллекции.
Развяжение будет сделано службой.
Чтобы помочь пользователю в предварительной проверке операции, клиент может позвонить, если для свойства validateOnly за установлено истинное имя.

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
Операция перемещения запускается после перемещенияResources в moveState "MovePending" или "MoveFailed", при успешном завершении перемещениеResource moveState сделает переход на CommitPending.
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

