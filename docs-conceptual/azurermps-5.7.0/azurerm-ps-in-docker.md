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
ms.sourcegitcommit: cb1fd248920d7efca67bd6c738a3b47206df7890
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/13/2018
ms.locfileid: "39024619"
---
# <a name="run-azure-powershell-in-a-docker-container"></a><span data-ttu-id="1ddc0-103">Запуск Azure PowerShell в контейнере Docker</span><span class="sxs-lookup"><span data-stu-id="1ddc0-103">Run Azure PowerShell in a Docker container</span></span>

<span data-ttu-id="1ddc0-104">Существует набор образов Docker, содержащих Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-104">There are a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="1ddc0-105">Доступны два типа контейнеров: со стандартной оболочкой PowerShell в Windows и PowerShell Core в Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-105">Two types of containers are available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="1ddc0-106">Среда</span><span class="sxs-lookup"><span data-stu-id="1ddc0-106">Environment</span></span> | <span data-ttu-id="1ddc0-107">Образ Docker</span><span class="sxs-lookup"><span data-stu-id="1ddc0-107">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="1ddc0-108">PowerShell в среде Windows</span><span class="sxs-lookup"><span data-stu-id="1ddc0-108">PowerShell on Windows</span></span> | [<span data-ttu-id="1ddc0-109">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="1ddc0-109">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="1ddc0-110">PowerShell Core в среде Windows</span><span class="sxs-lookup"><span data-stu-id="1ddc0-110">PowerShell Core on Windows</span></span> | [<span data-ttu-id="1ddc0-111">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="1ddc0-111">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="1ddc0-112">PowerShell Core в среде Linux</span><span class="sxs-lookup"><span data-stu-id="1ddc0-112">PowerShell Core on Linux</span></span> | [<span data-ttu-id="1ddc0-113">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="1ddc0-113">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="1ddc0-114">Для запуска любого из этих контейнеров используйте `docker run -it $ImageName`, чтобы получить интерактивный терминал.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-114">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="1ddc0-115">Например, чтобы запустить контейнер с PowerShell Core в среде Linux, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1ddc0-115">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="1ddc0-116">Чтобы запустить контейнер Windows в Docker, в качестве ОС узла должна использоваться ОС Windows, а Docker необходимо настроить для запуска контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-116">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="1ddc0-117">Дополнительные сведения о переключении между средами Windows и Linux в Docker см. в документации по Docker [о переключении между контейнерами Windows и Linux](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span><span class="sxs-lookup"><span data-stu-id="1ddc0-117">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>

## <a name="use-a-powershell-core-container"></a><span data-ttu-id="1ddc0-118">Использование контейнеров PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="1ddc0-118">Use a PowerShell Core container</span></span>

<span data-ttu-id="1ddc0-119">В таких контейнерах уже установлены оболочка PowerShell Core версии 6 и модуль `AzureRM.NetCore`.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-119">The PowerShell Core containers come with PowerShell Core v6 and the `AzureRM.NetCore` module pre-installed.</span></span> <span data-ttu-id="1ddc0-120">Запустите командлет [Import-Module](/powershell/module/microsoft.powershell.core/import-module) и войдите с помощью своей учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-120">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM.NetCore
Connect-AzureRmAccount
```

## <a name="use-the-windows-container-with-powershell"></a><span data-ttu-id="1ddc0-121">Использование контейнеров Windows и PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ddc0-121">Use the Windows container with PowerShell</span></span>

<span data-ttu-id="1ddc0-122">В контейнерах Windows уже установлен модуль `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-122">The Windows container has the `AzureRM` module pre-installed.</span></span> <span data-ttu-id="1ddc0-123">Запустите командлет [Import-Module](/powershell/module/microsoft.powershell.core/import-module) и войдите с помощью своей учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="1ddc0-123">Run the [Import-Module](/powershell/module/microsoft.powershell.core/import-module) cmdlet and then sign in with your Azure account:</span></span>

```powershell
Import-Module AzureRM
Connect-AzureRmAccount
```