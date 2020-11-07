---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 1ab1690d3c5fccca2994abc4958f3cf7e6a4e52d
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93719836"
---
# AZ. StorageSync Module
## Nописание
Командлеты в модуле синхронизации хранилища позволяют управлять операциями, относящимися к синхронизации файлов Azure в PowerShell.

## Командлеты AZ. StorageSync
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Эта команда перечисляет все конечные точки облака в заданной группе синхронизации.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Эта команда выводит список всех групп синхронизации в заданной службе синхронизации хранилища.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Эта команда перечисляет все серверы, зарегистрированные для указанной службы синхронизации хранилища.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Эта команда перечисляет все конечные точки сервера в заданной группе синхронизации.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Эта команда выводит список всех служб синхронизации хранилища в заданной области подписки или группы ресурсов.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Проверка наличия потенциальных проблем с совместимостью системы и синхронизации файлов Azure.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Эта команда повторно вызывает все многоуровневые файлы на локальный диск.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Эта команда создает облачную конечную точку синхронизации файлов Azure в группе синхронизации.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Эта команда создает новую группу синхронизации в указанной службе синхронизации хранилища.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Эта команда создает новую конечную точку сервера на зарегистрированном сервере. Это позволяет заданному пути на сервере запустить синхронизацию файлов с другими конечными точками в группе "Синхронизация".

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Эта команда создает новую службу синхронизации хранилища в группе ресурсов.

### [Регистрация — AzStorageSyncServer](Register-AzStorageSyncServer.md)
Эта команда регистрирует сервер для службы синхронизации хранилища, который создает отношение доверия. Вы можете использовать PowerShell или портал Azure для настройки синхронизации на этом сервере.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Эта команда удалит указанную облачную конечную точку из группы синхронизации. Без хотя бы одной конечной точки облака нельзя синхронизировать другие конечные точки сервера в этой группе синхронизации.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Эта команда удалит указанную группу синхронизации.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Эта команда удалит указанную конечную точку сервера. Синхронизация с этим расположением будет немедленно остановлена.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Эта команда удалит указанную службу синхронизации хранилища.

### [Сброс — AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Используется только для устранения неполадок. Эта команда выполняет откат сертификата сервера синхронизации хранилища, используемого для описания удостоверения сервера для службы синхронизации хранилища.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Эта команда позволяет вносить изменения в регулируемых параметрах конечной точки сервера.

### [Отмена регистрации — AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Предупреждение: Отмена регистрации сервера приводит к каскадному удалению всех конечных точек сервера на этом сервере. Эта команда отменит регистрацию сервера в службе синхронизации хранилища.