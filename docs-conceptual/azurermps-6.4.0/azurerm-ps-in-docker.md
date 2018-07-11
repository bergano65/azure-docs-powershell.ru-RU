---
title: Запуск Azure PowerShell в контейнере Docker
description: Сведения о том, как запустить Azure PowerShell в контейнере Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: b224beb95809d0e48c6f1dd5985de45b3b4df816
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406365"
---
## <a name="run-azure-powershell-in-a-docker-container"></a>Запуск Azure PowerShell в контейнере Docker

Существует набор образов Docker, содержащих Azure PowerShell. Доступны два типа контейнеров: со стандартной оболочкой PowerShell в Windows и PowerShell Core в Windows или Linux.

| Среда | Образ Docker |
|-------------|--------------|
| PowerShell в среде Windows | [azuresdk/azure-powershell](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| PowerShell Core в среде Windows | [azuresdk/azure-powershell-core:nanoserver](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| PowerShell Core в среде Linux | [azuresdk/azure-powershell-core:latest](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

Для запуска любого из этих контейнеров используйте `docker run -it $ImageName`, чтобы получить интерактивный терминал. Например, чтобы запустить контейнер с PowerShell Core в среде Linux, используйте следующую команду:

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> Чтобы запустить контейнер Windows в Docker, в качестве ОС узла должна использоваться ОС Windows, а Docker необходимо настроить для запуска контейнеров Windows. Дополнительные сведения о переключении между средами Windows и Linux в Docker см. в документации по Docker [о переключении между контейнерами Windows и Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).

## <a name="use-a-powershell-core-container"></a>Использование контейнеров PowerShell Core

В таких контейнерах уже установлены оболочка PowerShell Core версии 6 и модуль `AzureRM.NetCore`. Запустите командлет [Import-Module](/powershell/module/microsoft.powershell.core/import-module) и войдите с помощью своей учетной записи Azure.

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a>Использование контейнеров Windows и PowerShell

В контейнерах Windows уже установлен модуль `AzureRM`. Запустите командлет [Import-Module](/powershell/module/microsoft.powershell.core/import-module) и войдите с помощью своей учетной записи Azure.

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```