---
title: Запуск Azure PowerShell в контейнере Docker
description: Сведения о том, как запустить Azure PowerShell в контейнере Docker.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: 656c58fbb7cafb539736a0083d6aed1f46b7b98d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110336"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="06ae6-103">Запуск Azure PowerShell в контейнере Docker</span><span class="sxs-lookup"><span data-stu-id="06ae6-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="06ae6-104">Существует набор образов Docker, содержащих Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06ae6-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="06ae6-105">Доступны два типа контейнеров: со стандартной оболочкой PowerShell в Windows и PowerShell Core в Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="06ae6-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="06ae6-106">Среда</span><span class="sxs-lookup"><span data-stu-id="06ae6-106">Environment</span></span> | <span data-ttu-id="06ae6-107">Образ Docker</span><span class="sxs-lookup"><span data-stu-id="06ae6-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="06ae6-108">PowerShell в среде Windows</span><span class="sxs-lookup"><span data-stu-id="06ae6-108">PowerShell on Windows</span></span> | [<span data-ttu-id="06ae6-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="06ae6-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="06ae6-110">PowerShell Core в среде Windows</span><span class="sxs-lookup"><span data-stu-id="06ae6-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="06ae6-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="06ae6-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="06ae6-112">PowerShell Core в среде Linux</span><span class="sxs-lookup"><span data-stu-id="06ae6-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="06ae6-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="06ae6-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="06ae6-114">Для запуска любого из этих контейнеров используйте `docker run -it $ImageName`, чтобы получить интерактивный терминал.</span><span class="sxs-lookup"><span data-stu-id="06ae6-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="06ae6-115">Например, чтобы запустить контейнер с PowerShell Core в среде Linux, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="06ae6-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="06ae6-116">Чтобы запустить контейнер Windows в Docker, в качестве ОС узла должна использоваться ОС Windows, а Docker необходимо настроить для запуска контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="06ae6-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="06ae6-117">Дополнительные сведения о переключении между средами Windows и Linux в Docker см. в документации по Docker [о переключении между контейнерами Windows и Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="06ae6-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="06ae6-118">Использование контейнеров PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="06ae6-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="06ae6-119">В таких контейнерах уже установлены оболочка PowerShell Core версии 6 и модуль `AzureRM.NetCore`.</span><span class="sxs-lookup"><span data-stu-id="06ae6-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="06ae6-120">Запустите командлет [Import-Module](/powershell/module/microsoft.powershell.core/import-module) и войдите с помощью своей учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="06ae6-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="06ae6-121">Использование контейнеров Windows и PowerShell</span><span class="sxs-lookup"><span data-stu-id="06ae6-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="06ae6-122">В контейнерах Windows уже установлен модуль `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="06ae6-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="06ae6-123">Запустите командлет [Import-Module](/powershell/module/microsoft.powershell.core/import-module) и войдите с помощью своей учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="06ae6-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```