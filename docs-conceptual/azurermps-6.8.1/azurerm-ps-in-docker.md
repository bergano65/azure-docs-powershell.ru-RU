---
title: Запуск Azure PowerShell в контейнере Docker
description: Сведения о том, как запустить Azure PowerShell в контейнере Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 27ac176d8bd0b142b7740b2ba6793edb500a8af3
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383572"
---
# <a name="run-azure-powershell-in-a-docker-container"></a>Запуск Azure PowerShell в контейнере Docker

Чтобы без проблем запускать Azure PowerShell в переносной среде, корпорация Майкрософт публикует образы Docker с предварительной установкой Azure PowerShell. Эти образы позволяют использовать PowerShell Core в гостевой ОС Linux либо PowerShell Core или PowerShell 5 в гостевой ОС Windows.

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
