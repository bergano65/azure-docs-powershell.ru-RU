---
title: Использование учетных данных пользователя в разных сеансах PowerShell
description: Узнайте, как использовать учетные данные Azure и другие сведения в нескольких сеансах PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8702de48429482748939fb1a43ff911bed15f6c0
ms.sourcegitcommit: c0f1ef7fd165e5f57dd2b753265510f111356c5f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2019
ms.locfileid: "54071919"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="8caf3-103">Использование учетных данных пользователя в разных сеансах PowerShell</span><span class="sxs-lookup"><span data-stu-id="8caf3-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="8caf3-104">В Azure PowerShell существует функция **автосохранения контекста Azure**, которая предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="8caf3-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="8caf3-105">хранение учетных данных для входа для повторного использования в новых сеансах PowerShell;</span><span class="sxs-lookup"><span data-stu-id="8caf3-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="8caf3-106">упрощенное использование фоновых задач для запуска долго выполняющихся командлетов;</span><span class="sxs-lookup"><span data-stu-id="8caf3-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="8caf3-107">переключение между учетными записями, подписками и средами без необходимости выполнять отдельный вход;</span><span class="sxs-lookup"><span data-stu-id="8caf3-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="8caf3-108">одновременное выполнение задач с использованием разных учетных данных и подписок в рамках одного сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8caf3-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="8caf3-109">Определенные контексты Azure</span><span class="sxs-lookup"><span data-stu-id="8caf3-109">Azure contexts defined</span></span>

<span data-ttu-id="8caf3-110">*Контекст Azure* — это набор сведений, которые определяют целевой объект для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8caf3-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="8caf3-111">Контекст состоит из пяти частей:</span><span class="sxs-lookup"><span data-stu-id="8caf3-111">The context consists of five parts:</span></span>

- <span data-ttu-id="8caf3-112">*Учетная запись* — имя пользователя или субъекта-службы, которое используется для аутентификации при обмене данными со средой Azure.</span><span class="sxs-lookup"><span data-stu-id="8caf3-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="8caf3-113">*Подписка* — подписка Azure с используемыми ресурсами.</span><span class="sxs-lookup"><span data-stu-id="8caf3-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="8caf3-114">*Клиент* — клиент Azure Active Directory, который содержит вашу подписку.</span><span class="sxs-lookup"><span data-stu-id="8caf3-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="8caf3-115">Клиенты являются более важными при аутентификации субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="8caf3-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="8caf3-116">*Среда* — определяемое облако Azure (обычно это глобальное облако Azure).</span><span class="sxs-lookup"><span data-stu-id="8caf3-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="8caf3-117">Кроме того, параметр среды позволяет определять национальные и локальные (Azure Stack) облака, а также облака для государственных организаций.</span><span class="sxs-lookup"><span data-stu-id="8caf3-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="8caf3-118">*Учетные данные* — сведения, которые используются в Azure, чтобы выполнить идентификацию и авторизацию для доступа к ресурсам в Azure.</span><span class="sxs-lookup"><span data-stu-id="8caf3-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="8caf3-119">В последней версии Azure PowerShell контексты Azure автоматически сохраняются при каждом открытии нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8caf3-119">With the latest version of Azure PowerShell, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="8caf3-120">Автоматическое сохранение контекста для следующего входа</span><span class="sxs-lookup"><span data-stu-id="8caf3-120">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="8caf3-121">В Azure PowerShell данные контекста автоматически сохраняются между сеансами.</span><span class="sxs-lookup"><span data-stu-id="8caf3-121">Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="8caf3-122">Чтобы PowerShell не сохранял учетные данные и данные контекста, используйте `Disable-AzContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="8caf3-122">To set PowerShell to forget your context and credentials, use `Disable-AzContextAutoSave`.</span></span> <span data-ttu-id="8caf3-123">Если сохранение контекста отключено, вам нужно будет каждый раз при открытии сеанса PowerShell входить в Azure.</span><span class="sxs-lookup"><span data-stu-id="8caf3-123">With context saving disabled, you'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="8caf3-124">Чтобы разрешить Azure PowerShell запоминать контекст после закрытия сеанса PowerShell, используйте `Enable-AzContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="8caf3-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzContextAutosave`.</span></span> <span data-ttu-id="8caf3-125">Учетные данные и данные контекста автоматически сохраняются в специальной скрытой папке в каталоге пользователя (`$env:USERPROFILE\.Azure` — на Windows и `$HOME/.Azure` — на других платформах).</span><span class="sxs-lookup"><span data-stu-id="8caf3-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="8caf3-126">Каждый новый сеанс PowerShell обращается к контексту, который использовался в последнем сеансе.</span><span class="sxs-lookup"><span data-stu-id="8caf3-126">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="8caf3-127">Командлеты, которые помогают управлять контекстами Azure, также предоставляют удобные средства.</span><span class="sxs-lookup"><span data-stu-id="8caf3-127">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="8caf3-128">С их помощью вы можете применить изменения как для текущего сеанса PowerShell (область `Process`), так и для всех сеансов PowerShell (область `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="8caf3-128">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="8caf3-129">Эти параметры подробно описаны в разделе [Использование областей контекстов](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="8caf3-129">These options are discussed in more detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="8caf3-130">Выполнение командлетов Azure PowerShell как фоновых заданий</span><span class="sxs-lookup"><span data-stu-id="8caf3-130">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="8caf3-131">Функция **автосохранения контекста Azure** также позволяет использовать контекст с фоновыми заданиями PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8caf3-131">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="8caf3-132">PowerShell позволяет запускать и отслеживать долго выполняющиеся задачи как фоновые задания. Для этого вам не нужно дожидаться завершения их выполнения.</span><span class="sxs-lookup"><span data-stu-id="8caf3-132">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="8caf3-133">Чтобы использовать в фоновых заданиях учетные данные, можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="8caf3-133">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="8caf3-134">Передать контекст как аргумент.</span><span class="sxs-lookup"><span data-stu-id="8caf3-134">Passing the context as an argument</span></span>

  <span data-ttu-id="8caf3-135">Большинство командлетов AzureRM позволяют передавать контекст как параметр.</span><span class="sxs-lookup"><span data-stu-id="8caf3-135">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="8caf3-136">Передать контекст в фоновое задание можно так:</span><span class="sxs-lookup"><span data-stu-id="8caf3-136">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzContext)
  ```

- <span data-ttu-id="8caf3-137">Использовать контекст по умолчанию со включенной функцией автосохранения</span><span class="sxs-lookup"><span data-stu-id="8caf3-137">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="8caf3-138">Если включить функцию **автосохранения контекста**, фоновые задания будут автоматически использовать сохраненный контекст по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8caf3-138">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzVm [... Additional parameters ...]}
  ```

<span data-ttu-id="8caf3-139">Если вам нужно узнать выходные данные фоновой задачи, используйте `Get-Job`, чтобы проверить состояние задания, и `Wait-Job`, чтобы дождаться завершения задания.</span><span class="sxs-lookup"><span data-stu-id="8caf3-139">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="8caf3-140">Используйте `Receive-Job`, чтобы записать или отобразить выходные данные фонового задания.</span><span class="sxs-lookup"><span data-stu-id="8caf3-140">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="8caf3-141">См. дополнительные сведения о [заданиях](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="8caf3-141">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="8caf3-142">Создание, выбор, переименование и удаление контекстов</span><span class="sxs-lookup"><span data-stu-id="8caf3-142">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="8caf3-143">Чтобы создать контекст, нужно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="8caf3-143">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="8caf3-144">Командлет `Connect-AzAccount` (или его псевдоним `Login-AzAccount`) определяет контекст по умолчанию, который будет использоваться командлетами Azure PowerShell. Он также обеспечивает доступ к любому клиенту или подписке в рамках разрешений, предоставляемых вашими учетными данными.</span><span class="sxs-lookup"><span data-stu-id="8caf3-144">The `Connect-AzAccount` cmdlet (or its alias, `Login-AzAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="8caf3-145">Чтобы добавить новый контекст после входа, используйте командлет `Set-AzContext` (или его псевдоним `Select-AzSubscription`).</span><span class="sxs-lookup"><span data-stu-id="8caf3-145">To add a new context after sign-in, use `Set-AzContext` (or its alias, `Select-AzSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="8caf3-146">В примере выше мы добавили новый контекст для подписки "Contoso Subscription 1", используя текущие учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8caf3-146">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="8caf3-147">Новый контекст называется "Contoso1".</span><span class="sxs-lookup"><span data-stu-id="8caf3-147">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="8caf3-148">Если вы не укажете имя для контекста, будет использоваться имя по умолчанию на основе идентификатора учетной записи и подписки.</span><span class="sxs-lookup"><span data-stu-id="8caf3-148">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="8caf3-149">Чтобы переименовать существующий контекста, используйте командлет `Rename-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="8caf3-149">To rename an existing context, use the `Rename-AzContext` cmdlet.</span></span> <span data-ttu-id="8caf3-150">Например: </span><span class="sxs-lookup"><span data-stu-id="8caf3-150">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="8caf3-151">В этом примере мы изменяем стандартное имя контекста `[user1@contoso.org; 123456-7890-1234-564321]` на простое имя "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="8caf3-151">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="8caf3-152">Командлеты, которые управляют контекстами, также поддерживают заполнение нажатием клавиши TAB. Это позволяет быстро выбрать контекст.</span><span class="sxs-lookup"><span data-stu-id="8caf3-152">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="8caf3-153">Наконец, чтобы удалить контекст, используйте командлет `Remove-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="8caf3-153">Finally, to remove a context, use the `Remove-AzContext` cmdlet.</span></span>  <span data-ttu-id="8caf3-154">Например: </span><span class="sxs-lookup"><span data-stu-id="8caf3-154">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzContext Contoso2
```

<span data-ttu-id="8caf3-155">Удаление контекста с именем "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="8caf3-155">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="8caf3-156">Этот контекст можно создать повторно с помощью командлета `Set-AzContext`.</span><span class="sxs-lookup"><span data-stu-id="8caf3-156">You can recreate this context using `Set-AzContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="8caf3-157">Удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="8caf3-157">Removing credentials</span></span>

<span data-ttu-id="8caf3-158">Вы можете удалить все учетные данные и связанные контексты пользователя или субъекта-службы с помощью командлета `Disconnect-AzAccount` (или его псевдонима `Logout-AzAccount`).</span><span class="sxs-lookup"><span data-stu-id="8caf3-158">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzAccount` (also known as `Logout-AzAccount`).</span></span> <span data-ttu-id="8caf3-159">Выполняемый без параметров командлет `Disconnect-AzAccount` удаляет все учетные данные и контексты, связанные с пользователем или субъектом-службой в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="8caf3-159">When executed without parameters, the `Disconnect-AzAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="8caf3-160">Чтобы связать с контекстом определенный субъект, вы можете передать имя пользователя, имя субъекта-службы или сам контекст.</span><span class="sxs-lookup"><span data-stu-id="8caf3-160">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="8caf3-161">Использование областей контекстов</span><span class="sxs-lookup"><span data-stu-id="8caf3-161">Using context scopes</span></span>

<span data-ttu-id="8caf3-162">Иногда нужно выбрать, изменить или удалить контекст в сеансе PowerShell, не влияя на другие сеансы.</span><span class="sxs-lookup"><span data-stu-id="8caf3-162">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="8caf3-163">Чтобы изменить стандартное поведение командлетов, управляющих контекстом, используйте параметр `Scope`.</span><span class="sxs-lookup"><span data-stu-id="8caf3-163">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="8caf3-164">Область `Process` переопределяет стандартное поведение, ограничивая его действие текущим сеансом.</span><span class="sxs-lookup"><span data-stu-id="8caf3-164">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="8caf3-165">И наоборот, область `CurrentUser` изменяет контекст во всех сеансах, а не только в текущем.</span><span class="sxs-lookup"><span data-stu-id="8caf3-165">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="8caf3-166">Например, вот как можно изменить контекст по умолчанию в текущем сеансе PowerShell, не влияя на другие окна, или изменить контекст, который будет использоваться при следующем открытии сеанса:</span><span class="sxs-lookup"><span data-stu-id="8caf3-166">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="8caf3-167">Запоминание параметра автосохранения контекста</span><span class="sxs-lookup"><span data-stu-id="8caf3-167">How the context autosave setting is remembered</span></span>

<span data-ttu-id="8caf3-168">Параметр автосохранения контекста сохраняется в каталоге пользователя Azure PowerShell (`$env:USERPROFILE\.Azure` — на Windows и `$HOME/.Azure` — на других платформах).</span><span class="sxs-lookup"><span data-stu-id="8caf3-168">The context AutoSave setting is saved to the user Azure PowerShell directory (`$env:USERPROFILE\.Azure` on Windows, and `$HOME/.Azure` on other platforms).</span></span> <span data-ttu-id="8caf3-169">На некоторых компьютерах учетные записи могут не иметь доступ к этому каталогу.</span><span class="sxs-lookup"><span data-stu-id="8caf3-169">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="8caf3-170">В таких случаях можно использовать переменную среды</span><span class="sxs-lookup"><span data-stu-id="8caf3-170">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="8caf3-171">Если задано значение true, контекст сохраняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="8caf3-171">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="8caf3-172">Если задано значение false, контекст не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="8caf3-172">If set to 'false', the context isn't saved.</span></span>

## <a name="context-management-cmdlets"></a><span data-ttu-id="8caf3-173">Командлеты управления контекстом</span><span class="sxs-lookup"><span data-stu-id="8caf3-173">Context management cmdlets</span></span>

- <span data-ttu-id="8caf3-174">[Enable-AzContextAutosave][enable] — возможность сохранять контекст для использования в разных сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8caf3-174">[Enable-AzContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="8caf3-175">Любые изменения влияют на глобальный контекст.</span><span class="sxs-lookup"><span data-stu-id="8caf3-175">Any changes alter the global context.</span></span>
- <span data-ttu-id="8caf3-176">[Disable-AzContextAutosave][disable] — отключение автосохранения контекста.</span><span class="sxs-lookup"><span data-stu-id="8caf3-176">[Disable-AzContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="8caf3-177">Для работы с новым сеансом PowerShell нужно будет выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="8caf3-177">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="8caf3-178">[Select-AzContext][select] — выбор контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8caf3-178">[Select-AzContext][select] - Select a context as the default.</span></span> <span data-ttu-id="8caf3-179">Все командлеты используют для аутентификации учетные данные из этого контекста.</span><span class="sxs-lookup"><span data-stu-id="8caf3-179">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="8caf3-180">[Disconnect-AzAccount][remove-cred] — удаление всех учетных данных и контекстов, связанных с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="8caf3-180">[Disconnect-AzAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="8caf3-181">[Remove-AzContext][remove-context] — удаление именованного контекста.</span><span class="sxs-lookup"><span data-stu-id="8caf3-181">[Remove-AzContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="8caf3-182">[Rename-AzContext][rename] — переименование существующего контекста.</span><span class="sxs-lookup"><span data-stu-id="8caf3-182">[Rename-AzContext][rename] - Rename an existing context.</span></span>
- <span data-ttu-id="8caf3-183">[Add-AzAccount][login] — возможность определения входа на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8caf3-183">[Add-AzAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="8caf3-184">После аутентификации разрешено присваивать имя контексту по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8caf3-184">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="8caf3-185">[Import-AzContext][import] — возможность входа на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8caf3-185">[Import-AzContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="8caf3-186">[Set-AzContext][set-context] — возможность выбора существующих именованных контекстов и изменения области на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="8caf3-186">[Set-AzContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/az.accounts/Enable-AzureRmContextAutosave
[disable]: /powershell/module/az.accounts/Disable-AzContextAutosave
[select]: /powershell/module/az.accounts/Select-AzContext
[remove-cred]: /powershell/module/az.accounts/Disconnect-AzAccount
[remove-context]: /powershell/module/az.accounts/Remove-AzContext
[rename]: /powershell/module/az.accounts/Rename-AzContext

<!-- Updated cmdlets -->
[login]: /powershell/module/az.accounts/Connect-AzAccount
[import]:  /powershell/module/az.accounts/Import-AzContext
[set-context]: /powershell/module/az.accounts/Set-AzContext
