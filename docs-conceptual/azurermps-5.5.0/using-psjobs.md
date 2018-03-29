---
title: "Выполнение командлетов в параллельном режиме с помощью заданий PowerShell"
description: "Как выполнять командлеты в параллельном режиме с помощью параметра -AsJob."
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/11/2017
ms.openlocfilehash: 0a445a7db84c8deb6518b826b4096983669c5961
ms.sourcegitcommit: 20af779cd523c758d40e23d60eb989a4ef982d5c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2018
---
# <a name="running-cmdlets-in-parallel-using-powershell-jobs"></a><span data-ttu-id="d1408-103">Выполнение командлетов в параллельном режиме с помощью заданий PowerShell</span><span class="sxs-lookup"><span data-stu-id="d1408-103">Running cmdlets in parallel using PowerShell jobs</span></span>

<span data-ttu-id="d1408-104">PowerShell поддерживает выполнение асинхронных действий с помощью [заданий PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="d1408-104">PowerShell supports asynchronous action with [PowerShell Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>
<span data-ttu-id="d1408-105">Azure PowerShell в значительной степени зависит от выполнения и ожидания сетевых вызовов в Azure.</span><span class="sxs-lookup"><span data-stu-id="d1408-105">Azure PowerShell is heavily dependent on making, and waiting for, network calls to Azure.</span></span> <span data-ttu-id="d1408-106">Разработчики часто пытаются выполнить несколько неблокирующих вызовов в Azure в рамках одного скрипта или создать ресурсы Azure в REPL без блокировки текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="d1408-106">As a developer, you may often find yourself looking to make multiple non-blocking calls to Azure in a script, or you may find that you want to create Azure resources in the REPL without blocking the current session.</span></span> <span data-ttu-id="d1408-107">Для решения таких задач Azure PowerShell предоставляет поддержку [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) первого класса.</span><span class="sxs-lookup"><span data-stu-id="d1408-107">To address these needs, Azure PowerShell provides first-class [PSJob](/powershell/module/microsoft.powershell.core/about/about_jobs) support.</span></span>

## <a name="context-persistence-and-psjobs"></a><span data-ttu-id="d1408-108">Сохранение контекста и PSJobs</span><span class="sxs-lookup"><span data-stu-id="d1408-108">Context Persistence and PSJobs</span></span>

<span data-ttu-id="d1408-109">Задания PSJobs выполняются в рамках отдельных процессов. Это означает, что сведения о подключении к Azure необходимо правильно передавать в задания, которые вы создаете.</span><span class="sxs-lookup"><span data-stu-id="d1408-109">PSJobs are run in separate processes, which means that information about your Azure connection must be properly shared with the jobs you create.</span></span> <span data-ttu-id="d1408-110">При подключении учетной записи Azure к сеансу PowerShell с помощью `Login-AzureRmAccount` можно передать заданию контекст.</span><span class="sxs-lookup"><span data-stu-id="d1408-110">Upon connecting your Azure account to your PowerShell session with `Login-AzureRmAccount`, you can pass the context to a job.</span></span>

```powershell
$creds = Get-Credential
$job = Start-Job { param($context,$vmadmin) New-AzureRmVM -Name MyVm -AzureRmContext $context -Credential $vmadmin} -Arguments (Get-AzureRmContext),$creds
```

<span data-ttu-id="d1408-111">Но если вы настроили для контекста автоматическое сохранение с помощью `Enable-AzureRmContextAutosave`, то контекст автоматически будет доступными для создаваемых заданий.</span><span class="sxs-lookup"><span data-stu-id="d1408-111">However, if you have chosen to have your context automatically saved with `Enable-AzureRmContextAutosave`, the context is automatically shared with any jobs you create.</span></span>

```powershell
Enable-AzureRmContextAutosave
$creds = Get-Credential
$job = Start-Job { param($vmadmin) New-AzureRmVM -Name MyVm -Credential $vmadmin} -Arguments $creds
```

## <a name="automatic-jobs-with--asjob"></a><span data-ttu-id="d1408-112">Выполнение автоматических заданий с помощью `-AsJob`</span><span class="sxs-lookup"><span data-stu-id="d1408-112">Automatic Jobs with `-AsJob`</span></span>

<span data-ttu-id="d1408-113">Для удобства Azure PowerShell также предоставляет параметр `-AsJob` для некоторых длительно выполняющихся командлетов.</span><span class="sxs-lookup"><span data-stu-id="d1408-113">As a convenience, Azure PowerShell also provides an `-AsJob` switch on some long-running cmdlets.</span></span>
<span data-ttu-id="d1408-114">Параметр `-AsJob` еще больше упрощает создание PSJobs.</span><span class="sxs-lookup"><span data-stu-id="d1408-114">The `-AsJob` switch makes creating PSJobs even easier.</span></span>

```powershell
$creds = Get-Credential
$job = New-AzureRmVM -Name MyVm -Credential $creds -AsJob
```

<span data-ttu-id="d1408-115">Задание и ход выполнения можно проверить в любое время с помощью `Get-Job` и `Get-AzureRmVM`.</span><span class="sxs-lookup"><span data-stu-id="d1408-115">You can inspect the job and progress at any time with `Get-Job` and `Get-AzureRmVM`.</span></span>

```powershell
Get-Job $job
Get-AzureRmVM MyVm
```

```Output
Id Name                                       PSJobTypeName         State   HasMoreData Location  Command
-- ----                                       -------------         -----   ----------- --------  -------
1  Long Running Operation for 'New-AzureRmVM' AzureLongRunningJob`1 Running True        localhost New-AzureRmVM

ResourceGroupName    Name Location          VmSize  OsType     NIC ProvisioningState Zone
-----------------    ---- --------          ------  ------     --- ----------------- ----
MyVm                 MyVm   eastus Standard_DS1_v2 Windows    MyVm          Creating
```

<span data-ttu-id="d1408-116">По завершении процесса можно получить результат задания с помощью `Receive-Job`.</span><span class="sxs-lookup"><span data-stu-id="d1408-116">Subsequently, upon completion, you can obtain the result of the job with `Receive-Job`.</span></span>

> [!NOTE]
> <span data-ttu-id="d1408-117">`Receive-Job` возвращает результат от командлета так, как если бы флаг `-AsJob` отсутствовал.</span><span class="sxs-lookup"><span data-stu-id="d1408-117">`Receive-Job` returns the result from the cmdlet as if the `-AsJob` flag were not present.</span></span>
> <span data-ttu-id="d1408-118">Например, результат `Receive-Job` для `Do-Action -AsJob` будет того же типа, что и результат для `Do-Action`.</span><span class="sxs-lookup"><span data-stu-id="d1408-118">For example, the `Receive-Job` result of `Do-Action -AsJob` is of the same type as the result of `Do-Action`.</span></span>

```powershell
$vm = Receive-Job $job
$vm
```

```Output
ResourceGroupName        : MyVm
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyVm/providers/Microsoft.Compute/virtualMachines/MyVm
VmId                     : dff1f79e-a8f7-4664-ab72-0ec28b9fbb5b
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvmmyvm.eastus.cloudapp.azure.com
```

## <a name="example-scenarios"></a><span data-ttu-id="d1408-119">Примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="d1408-119">Example Scenarios</span></span>

<span data-ttu-id="d1408-120">Вы можете создать несколько виртуальных машин за один раз.</span><span class="sxs-lookup"><span data-stu-id="d1408-120">Create multiple VMs at once.</span></span>

```powershell
$creds = Get-Credential
# Create 10 jobs.
for($k = 0; $k -lt 10; $k++) {
    New-AzureRmVm -Name MyVm$k  -Credential $creds -AsJob
}

# Get all jobs and wait on them.
Get-Job | Wait-Job
"All jobs completed"
Get-AzureRmVM
```

<span data-ttu-id="d1408-121">В этом примере командлет `Wait-Job` приостанавливает работу скрипта во время выполнения задания.</span><span class="sxs-lookup"><span data-stu-id="d1408-121">In this example, the `Wait-Job` cmdlet causes the script to pause while jobs run.</span></span> <span data-ttu-id="d1408-122">Скрипт продолжит работу после выполнения всех заданий.</span><span class="sxs-lookup"><span data-stu-id="d1408-122">The script continues executing once all of the jobs have completed.</span></span> <span data-ttu-id="d1408-123">Это позволяет создать несколько заданий, выполняемых параллельно, а затем дождаться завершения, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="d1408-123">This allows you to create several jobs running in parallel then wait for completion before continuing.</span></span>

```Output
Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
2      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Running       True            localhost            New-AzureRmVM
2      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
3      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
4      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
5      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
6      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
7      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
8      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
9      Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
10     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
11     Long Running... AzureLongRun... Completed     True            localhost            New-AzureRmVM
All Jobs completed.

ResourceGroupName        Name   Location          VmSize  OsType           NIC ProvisioningState Zone
-----------------        ----   --------          ------  ------           --- ----------------- ----
MYVM                     MyVm     eastus Standard_DS1_v2 Windows          MyVm         Succeeded
MYVM0                   MyVm0     eastus Standard_DS1_v2 Windows         MyVm0         Succeeded
MYVM1                   MyVm1     eastus Standard_DS1_v2 Windows         MyVm1         Succeeded
MYVM2                   MyVm2     eastus Standard_DS1_v2 Windows         MyVm2         Succeeded
MYVM3                   MyVm3     eastus Standard_DS1_v2 Windows         MyVm3         Succeeded
MYVM4                   MyVm4     eastus Standard_DS1_v2 Windows         MyVm4         Succeeded
MYVM5                   MyVm5     eastus Standard_DS1_v2 Windows         MyVm5         Succeeded
MYVM6                   MyVm6     eastus Standard_DS1_v2 Windows         MyVm6         Succeeded
MYVM7                   MyVm7     eastus Standard_DS1_v2 Windows         MyVm7         Succeeded
MYVM8                   MyVm8     eastus Standard_DS1_v2 Windows         MyVm8         Succeeded
MYVM9                   MyVm9     eastus Standard_DS1_v2 Windows         MyVm9         Succeeded
```