---
title: Запуск Azure PowerShell в контейнере Docker
description: Сведения о том, как запустить Azure PowerShell в контейнере Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 0ed8f50abbcb2aa00192196f19004446dc696b5d
ms.sourcegitcommit: 6c38e86e16da99f65cd183c63e34f7176b121ab8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "47425267"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="18522-103">Запуск Azure PowerShell в контейнере Docker</span><span class="sxs-lookup"><span data-stu-id="18522-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="18522-104">Корпорация Майкрософт публикует образы Docker с предварительной установкой Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="18522-104">Microsoft publishes Docker images with Azure PowerShell pre-installed.</span></span> <span data-ttu-id="18522-105">Эти образы позволяют экспериментировать с Azure PowerShell или запускать это средство в изолированной среде.</span><span class="sxs-lookup"><span data-stu-id="18522-105">These images allow for experimenting with Azure PowerShell or running it in an isolated environment.</span></span> <span data-ttu-id="18522-106">Существуют образы под управлением PowerShell Core и PowerShell 5.</span><span class="sxs-lookup"><span data-stu-id="18522-106">There are images running both PowerShell Core and PowerShell 5.</span></span> 

| <span data-ttu-id="18522-107">Среда</span><span class="sxs-lookup"><span data-stu-id="18522-107">Environment</span></span> | <span data-ttu-id="18522-108">Образ Docker</span><span class="sxs-lookup"><span data-stu-id="18522-108">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="18522-109">PowerShell в среде Windows</span><span class="sxs-lookup"><span data-stu-id="18522-109">PowerShell on Windows</span></span> | [<span data-ttu-id="18522-110">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="18522-110">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="18522-111">PowerShell Core в среде Windows</span><span class="sxs-lookup"><span data-stu-id="18522-111">PowerShell Core on Windows</span></span> | [<span data-ttu-id="18522-112">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="18522-112">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="18522-113">PowerShell Core в среде Linux</span><span class="sxs-lookup"><span data-stu-id="18522-113">PowerShell Core on Linux</span></span> | [<span data-ttu-id="18522-114">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="18522-114">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="18522-115">Для запуска любого из этих контейнеров используйте `docker run -it $ImageName`, чтобы получить интерактивный терминал.</span><span class="sxs-lookup"><span data-stu-id="18522-115">To run any of these containers, use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="18522-116">Например, чтобы запустить контейнер Linux с PowerShell Core, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="18522-116">For example, to run a Linux container with PowerShell Core:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="18522-117">Чтобы запустить контейнер Windows в Docker, в качестве ОС узла должна использоваться ОС Windows, а Docker необходимо настроить для запуска контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="18522-117">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="18522-118">Дополнительные сведения о переключении между средами Windows и Linux в Docker см. в документации по Docker [о переключении между контейнерами Windows и Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="18522-118">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="18522-119">Использование контейнеров PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="18522-119">Use a PowerShell Core container</span></span>

<span data-ttu-id="18522-120">В таких контейнерах уже установлены оболочка PowerShell Core версии 6 и модуль `AzureRM.NetCore`.</span><span class="sxs-lookup"><span data-stu-id="18522-120">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="18522-121">Запустите командлет [Import-Module](/powershell/module/microsoft.powershell.core/import-module) и войдите с помощью своей учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="18522-121">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="18522-122">Использование контейнеров Windows и PowerShell</span><span class="sxs-lookup"><span data-stu-id="18522-122">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="18522-123">В контейнерах Windows уже установлен модуль `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="18522-123">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="18522-124">Запустите командлет [Import-Module](/powershell/module/microsoft.powershell.core/import-module) и войдите с помощью своей учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="18522-124">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```
