---
Module Name: Az.CloudService
Module Guid: a41eb61d-c5a1-4e9b-81a7-b8905fff7f2c
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Az.CloudService.md
ms.openlocfilehash: c9ab8aaefc7d97c7d1082b76b1dcef1546fe96d3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211924"
---
# Модуль Az.CloudService
## Описание
Microsoft Azure PowerShell: cmdlets CloudService

## Az.CloudService Cmdlets
### [Get-AzCloudService](Get-AzCloudService.md)
Отображение сведений об облачной службе.

### [Get-AzCloudServiceInstanceView](Get-AzCloudServiceInstanceView.md)
Возвращает состояние облачной службы.

### [Get-AzCloudServiceNetworkInterfaces](Get-AzCloudServiceNetworkInterfaces.md)
Получите сетевые интерфейсы облачной службы.

### [Get-AzCloudServicePublicIPAddress](Get-AzCloudServicePublicIPAddress.md)
Получите общедоступный IP-адрес облачной службы.

### [Get-AzCloudServiceRoleInstance](Get-AzCloudServiceRoleInstance.md)
Получает экземпляр роли из облачной службы.

### [Get-AzCloudServiceRoleInstanceRemoteDesktopFile](Get-AzCloudServiceRoleInstanceRemoteDesktopFile.md)
Получает файл удаленного рабочего стола для экземпляра роли в облачной службе.

### [Get-AzCloudServiceRoleInstanceView](Get-AzCloudServiceRoleInstanceView.md)
Извлекает сведения о состоянии времени запуска экземпляра роли в облачной службе.

### [Invoke-AzCloudServiceRebuild](Invoke-AzCloudServiceRebuild.md)
Перестроение экземпляров ролей переустановит операционную систему на основе экземпляров ролей веб-ролей или сотрудников и инициализирует используемые ими ресурсы хранилища.
Если вы не хотите инициализировать ресурсы хранилища, используйте экземпляры ролей Reimage.

### [Invoke-AzCloudServiceReimage](Invoke-AzCloudServiceReimage.md)
Асинхронная операция reimage переустановит операционную систему для экземпляров ролей веб-ролей или сотрудников.

### [Invoke-AzCloudServiceRoleInstanceRebuild](Invoke-AzCloudServiceRoleInstanceRebuild.md)
Асинхронная операция переустановки экземпляра роли переустановит операционную систему с экземплярами ролей веб-ролей или сотрудников и инициализирует используемые ими ресурсы хранилища.
Если вы не хотите инициализировать ресурсы хранилища, используйте экземпляр роли Reimage.

### [Invoke-AzCloudServiceRoleInstanceReimage](Invoke-AzCloudServiceRoleInstanceReimage.md)
Асинхронная операция "Экземпляр роли Reimage" переустановит операционную систему для экземпляров ролей веб-ролей или сотрудников.

### [New-AzCloudService](New-AzCloudService.md)
Создание или обновление облачной службы.
Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.

### [New-AzCloudServiceDiagnosticsExtension](New-AzCloudServiceDiagnosticsExtension.md)
Создание в памяти объекта для расширения диагностики

### [New-AzCloudServiceExtensionObject](New-AzCloudServiceExtensionObject.md)
Создание объекта в памяти для расширения

### [New-AzCloudServiceLoadBalancerConfigurationObject](New-AzCloudServiceLoadBalancerConfigurationObject.md)
Создание в памяти объекта для LoadBalancerConfiguration

### [New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject](New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md)
Создание в памяти объекта для LoadBalancerFrontendIPConfiguration

### [New-AzCloudServiceRemoteDesktopExtensionObject](New-AzCloudServiceRemoteDesktopExtensionObject.md)
Создание объекта в памяти для расширения удаленного рабочего стола

### [New-AzCloudServiceRoleProfilePropertiesObject](New-AzCloudServiceRoleProfilePropertiesObject.md)
Создание объекта в памяти для CloudServiceRoleProfileProperties

### [New-AzCloudServiceVaultSecretGroupObject](New-AzCloudServiceVaultSecretGroupObject.md)
Создание объекта в памяти для группы "Секретная группа"

### [Remove-AzCloudService](Remove-AzCloudService.md)
Удаляет облачную службу.

### [Remove-AzCloudServiceRoleInstance](Remove-AzCloudServiceRoleInstance.md)
Удаляет экземпляры ролей в облачной службе.

### [Restart-AzCloudService](Restart-AzCloudService.md)
Перезапуск одного или несколько экземпляров ролей в облачной службе.

### [Restart-AzCloudServiceRoleInstance](Restart-AzCloudServiceRoleInstance.md)
Асинхронная операция "Экземпляр перезагрузки" запрашивает перезагрузку экземпляра роли в облачной службе.

### [Set-AzCloudServiceUpdateDomain](Set-AzCloudServiceUpdateDomain.md)
Обновляет экземпляры роли в указанном домене обновления.

### [Start-AzCloudService](Start-AzCloudService.md)
Запускает облачную службу.

### [Stop-AzCloudService](Stop-AzCloudService.md)
Отключите облачную службу.
Обратите внимание на то, что ресурсы все еще закреплены, и с вас взимается плата за ресурсы.

### [Switch-AzCloudService](Switch-AzCloudService.md)
Обмен VIP-решениями между двумя балансирными балансами нагрузки облачной службы (расширенной поддержки).

### [Update-AzCloudService](Update-AzCloudService.md)
Создание или обновление облачной службы.
Обратите внимание, что некоторые свойства можно настроить только при создании облачной службы.

