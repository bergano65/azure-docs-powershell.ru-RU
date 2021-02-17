---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217196"
---
# Модуль Az.StorageSync
## Описание
С помощью командлетов в модуле синхронизации хранилища можно управлять операциями, касающимися синхронизации файлов Azure в PowerShell.

## Az.StorageSync Cmdlets
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Эта команда содержит список всех облачных конечных точек в заданной группе синхронизации.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Эта команда содержит список всех групп синхронизации в заданной службе синхронизации хранилища.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Эта команда содержит список всех серверов, зарегистрированных в данной службе синхронизации хранилища.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Эта команда содержит список всех конечных точек сервера в заданной группе синхронизации.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Эта команда содержит список всех служб синхронизации хранилища в рамках группы подписок и ресурсов.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Эту команду можно использовать для инициалов обнаружения изменений пространства имен вручную. Его можно настроить для всей папки, вемеской папки или набора файлов. Можно обнаружить не более 10 000 изменений. Если известна область изменений, ограничьте выполнение этой команды частями пространства имен, чтобы обнаружение изменений можно было быстро завершить в пределах 10 000 изменений.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Проверяет наличие возможных проблем совместимости между системой и службой Azure File Sync.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Эта команда отзывит все многоуровневые файлы на локальный диск.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Эта команда создает облачную конечную точку синхронизации файлов Azure в группе синхронизации.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Эта команда создает конечную точку сервера на зарегистрированном сервере. Это позволяет заданный путь на сервере начать синхронизацию файлов с другими конечными точками в группе синхронизации.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Эта команда создает новую службу синхронизации хранилища в группе ресурсов.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Эта команда задает службу синхронизации хранилища в группе ресурсов.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Эта команда регистрирует сервер в службе синхронизации хранилища, что создает отношение доверия. Затем для настройки синхронизации на этом сервере можно использовать PowerShell или портал Azure.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Эта команда удаляет указанную конечную точку облака из группы синхронизации. Без хотя бы одной облачной конечной точки другие конечные точки сервера в этой группе синхронизации не будут синхронизироваться.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Эта команда удалит указанную группу синхронизации.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Эта команда удалит указанную конечную точку сервера. Синхронизация с этой расположением остановится немедленно.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Эта команда удалит указанную службу синхронизации хранилища.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Используется только для устранения неполадок. Эта команда позволит свернуть сертификат сервера синхронизации хранилища, используемый для описания идентификаторов сервера, в службу синхронизации хранилища.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Эта команда позволяет вносить изменения в настраиваемые параметры конечной точки сервера.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Предупреждение. Если отрегистрить сервер, это приведет к каскадным удалениям всех конечных точек сервера на этом сервере. Эта команда отстранит регистрацию сервера из его службы синхронизации хранилища.

