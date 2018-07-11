---
title: Использование учетных данных пользователя в разных сеансах PowerShell
description: Узнайте, как использовать учетные данные Azure и другие сведения в нескольких сеансах PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: aa374c6e93124fb4b428aa8c4854f7424f494bff
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406698"
---
# <a name="persisting-user-credentials-across-powershell-sessions"></a><span data-ttu-id="f8382-103">Использование учетных данных пользователя в разных сеансах PowerShell</span><span class="sxs-lookup"><span data-stu-id="f8382-103">Persisting user credentials across PowerShell sessions</span></span>

<span data-ttu-id="f8382-104">Начиная с выпуска Azure PowerShell за сентябрь 2017 г. для командлетов Azure Resource Manager теперь доступна новая возможность — **автосохранение контекста Azure**.</span><span class="sxs-lookup"><span data-stu-id="f8382-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="f8382-105">Эта функция позволяет реализовать несколько новых сценариев, включая:</span><span class="sxs-lookup"><span data-stu-id="f8382-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="f8382-106">хранение учетных данных для входа для повторного использования в новых сеансах PowerShell;</span><span class="sxs-lookup"><span data-stu-id="f8382-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="f8382-107">упрощенное использование фоновых задач для запуска долго выполняющихся командлетов;</span><span class="sxs-lookup"><span data-stu-id="f8382-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="f8382-108">переключение между учетными записями, подписками и средами без необходимости выполнять отдельный вход;</span><span class="sxs-lookup"><span data-stu-id="f8382-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="f8382-109">одновременное выполнение задач с использованием разных учетных данных и подписок в рамках одного сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8382-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="f8382-110">Определенные контексты Azure</span><span class="sxs-lookup"><span data-stu-id="f8382-110">Azure contexts defined</span></span>

<span data-ttu-id="f8382-111">*Контекст Azure* — это набор сведений, которые определяют целевой объект для командлетов Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8382-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f8382-112">Контекст состоит из пяти частей:</span><span class="sxs-lookup"><span data-stu-id="f8382-112">The context consists of five parts:</span></span>

- <span data-ttu-id="f8382-113">*Учетная запись* — имя пользователя или субъекта-службы, которое используется для аутентификации при обмене данными со средой Azure.</span><span class="sxs-lookup"><span data-stu-id="f8382-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="f8382-114">*Подписка* — подписка Azure, которая содержит используемые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f8382-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="f8382-115">*Клиент* — клиент Azure Active Directory, который содержит вашу подписку.</span><span class="sxs-lookup"><span data-stu-id="f8382-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="f8382-116">Клиенты являются более важными при аутентификации субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="f8382-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="f8382-117">*Среда* — определяемое облако Azure (обычно это глобальное облако Azure).</span><span class="sxs-lookup"><span data-stu-id="f8382-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="f8382-118">Кроме того, параметр среды позволяет определять национальные и локальные (Azure Stack) облака, а также облака для государственных организаций.</span><span class="sxs-lookup"><span data-stu-id="f8382-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="f8382-119">*Учетные данные* — сведения, которые используются в Azure для идентификации и авторизации для доступа к ресурсам в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8382-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="f8382-120">В предыдущих версиях контекст Azure нужно было создавать при каждом открытии нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8382-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="f8382-121">Начиная с версии Azure PowerShell 4.4.0 вы можете включить автоматическое сохранение и повторное использование контекстов Azure при каждом открытии нового сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8382-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="f8382-122">Автоматическое сохранение контекста для следующего входа</span><span class="sxs-lookup"><span data-stu-id="f8382-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="f8382-123">По умолчанию Azure PowerShell не хранит данные контекста после закрытия сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8382-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="f8382-124">Чтобы разрешить Azure PowerShell запоминать контекст после закрытия сеанса PowerShell, используйте `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="f8382-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="f8382-125">Учетные данные и данные контекста автоматически сохраняются в специальной скрытой папке в каталоге пользователя (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="f8382-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="f8382-126">Таким образом, каждый новый сеанс PowerShell обращается к контексту, который использовался в ходе последнего сеанса.</span><span class="sxs-lookup"><span data-stu-id="f8382-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="f8382-127">Чтобы PowerShell не сохранял учетные данные и данные контекста, используйте `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="f8382-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="f8382-128">Для работы с новым сеансом PowerShell вам нужно будет входить в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8382-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="f8382-129">Командлеты, которые помогают управлять контекстами Azure, также предоставляют удобные средства.</span><span class="sxs-lookup"><span data-stu-id="f8382-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="f8382-130">С их помощью вы можете применить изменения как для текущего сеанса PowerShell (область `Process`), так и для всех сеансов PowerShell (область `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="f8382-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="f8382-131">Эти параметры будут подробно описаны в разделе [Использование областей контекстов](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="f8382-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="f8382-132">Выполнение командлетов Azure PowerShell как фоновых заданий</span><span class="sxs-lookup"><span data-stu-id="f8382-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="f8382-133">Функция **автосохранения контекста Azure** также позволяет использовать контекст с фоновыми заданиями PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8382-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="f8382-134">PowerShell позволяет запускать и отслеживать долго выполняющиеся задачи как фоновые задания. Для этого вам не нужно дожидаться завершения их выполнения.</span><span class="sxs-lookup"><span data-stu-id="f8382-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="f8382-135">Чтобы использовать в фоновых заданиях учетные данные, можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="f8382-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="f8382-136">Передать контекст как аргумент.</span><span class="sxs-lookup"><span data-stu-id="f8382-136">Passing the context as an argument</span></span>

  <span data-ttu-id="f8382-137">Большинство командлетов AzureRM позволяют передавать контекст как параметр.</span><span class="sxs-lookup"><span data-stu-id="f8382-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="f8382-138">Передать контекст в фоновое задание можно так:</span><span class="sxs-lookup"><span data-stu-id="f8382-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="f8382-139">Использовать контекст по умолчанию со включенной функцией автосохранения</span><span class="sxs-lookup"><span data-stu-id="f8382-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="f8382-140">Если включить функцию **автосохранения контекста**, фоновые задания будут автоматически использовать сохраненный контекст по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8382-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="f8382-141">Если вам нужно узнать выходные данные фоновой задачи, используйте `Get-Job`, чтобы проверить состояние задания, и `Wait-Job`, чтобы дождаться завершения задания.</span><span class="sxs-lookup"><span data-stu-id="f8382-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="f8382-142">Используйте `Receive-Job`, чтобы записать или отобразить выходные данные фонового задания.</span><span class="sxs-lookup"><span data-stu-id="f8382-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="f8382-143">См. дополнительные сведения о [заданиях](/powershell/module/microsoft.powershell.core/about/about_jobs).</span><span class="sxs-lookup"><span data-stu-id="f8382-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="f8382-144">Создание, выбор, переименование и удаление контекстов</span><span class="sxs-lookup"><span data-stu-id="f8382-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="f8382-145">Для создания контекста нужно войти в Azure.</span><span class="sxs-lookup"><span data-stu-id="f8382-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="f8382-146">Командлет `Connect-AzureRmAccount` (или его псевдоним `Login-AzureRmAccount`) определяет контекст по умолчанию, который будет использоваться последующими командлетами Azure PowerShell. Он также обеспечивает доступ к любому клиенту или подписке в рамках разрешений, предоставляемых вашими учетными данными для входа.</span><span class="sxs-lookup"><span data-stu-id="f8382-146">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="f8382-147">Чтобы добавить новый контекст после входа, используйте командлет `Set-AzureRmContext` (или его псевдоним `Select-AzureRmSubscription`).</span><span class="sxs-lookup"><span data-stu-id="f8382-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="f8382-148">В примере выше мы добавили новый контекст для подписки "Contoso Subscription 1", используя текущие учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f8382-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="f8382-149">Новый контекст называется "Contoso1".</span><span class="sxs-lookup"><span data-stu-id="f8382-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="f8382-150">Если вы не укажете имя для контекста, будет использоваться имя по умолчанию на основе идентификатора учетной записи и подписки.</span><span class="sxs-lookup"><span data-stu-id="f8382-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="f8382-151">Чтобы переименовать существующий контекста, используйте командлет `Rename-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="f8382-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="f8382-152">Например: </span><span class="sxs-lookup"><span data-stu-id="f8382-152">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="f8382-153">В этом примере мы изменяем стандартное имя контекста `[user1@contoso.org; 123456-7890-1234-564321]` на простое имя "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="f8382-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="f8382-154">Командлеты, которые управляют контекстами, также поддерживают заполнение нажатием клавиши TAB. Это позволяет быстро выбрать контекст.</span><span class="sxs-lookup"><span data-stu-id="f8382-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="f8382-155">Наконец, чтобы удалить контекст, используйте командлет `Remove-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="f8382-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="f8382-156">Например: </span><span class="sxs-lookup"><span data-stu-id="f8382-156">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="f8382-157">Удаление контекста с именем "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="f8382-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="f8382-158">Впоследствии этот контекст можно создать повторно с помощью командлета `Set-AzureRmContext`.</span><span class="sxs-lookup"><span data-stu-id="f8382-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="f8382-159">Удаление учетных данных</span><span class="sxs-lookup"><span data-stu-id="f8382-159">Removing credentials</span></span>

<span data-ttu-id="f8382-160">Вы можете удалить все учетные данные и связанные контексты пользователя или субъекта-службы с помощью командлета `Disconnect-AzureRmAccount` (или его псевдонима `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="f8382-160">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="f8382-161">Выполняемый без параметров командлет `Disconnect-AzureRmAccount` удаляет все учетные данные и контексты, связанные с пользователем или субъектом-службой в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="f8382-161">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="f8382-162">Чтобы связать с контекстом определенный субъект, вы можете передать имя пользователя, имя субъекта-службы или сам контекст.</span><span class="sxs-lookup"><span data-stu-id="f8382-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="f8382-163">Использование областей контекстов</span><span class="sxs-lookup"><span data-stu-id="f8382-163">Using context scopes</span></span>

<span data-ttu-id="f8382-164">Иногда нужно выбрать, изменить или удалить контекст в сеансе PowerShell, не влияя на другие сеансы.</span><span class="sxs-lookup"><span data-stu-id="f8382-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="f8382-165">Чтобы изменить стандартное поведение командлетов, управляющих контекстом, используйте параметр `Scope`.</span><span class="sxs-lookup"><span data-stu-id="f8382-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="f8382-166">Область `Process` переопределяет стандартное поведение, ограничивая его действие текущим сеансом.</span><span class="sxs-lookup"><span data-stu-id="f8382-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="f8382-167">И наоборот, область `CurrentUser` изменяет контекст во всех сеансах, а не только в текущем.</span><span class="sxs-lookup"><span data-stu-id="f8382-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="f8382-168">Например, вот как можно изменить контекст по умолчанию в текущем сеансе PowerShell, не влияя на другие окна, или изменить контекст, который будет использоваться при следующем открытии сеанса:</span><span class="sxs-lookup"><span data-stu-id="f8382-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="f8382-169">Запоминание параметра автосохранения контекста</span><span class="sxs-lookup"><span data-stu-id="f8382-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="f8382-170">Параметр автосохранения контекста сохраняется в каталоге пользователя Azure PowerShell (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="f8382-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="f8382-171">На некоторых компьютерах учетные записи могут не иметь доступ к этому каталогу.</span><span class="sxs-lookup"><span data-stu-id="f8382-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="f8382-172">В таких случаях можно использовать переменную среды</span><span class="sxs-lookup"><span data-stu-id="f8382-172">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="f8382-173">Если задано значение true, контекст сохраняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="f8382-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="f8382-174">Если задано значение false, контекст не сохраняется.</span><span class="sxs-lookup"><span data-stu-id="f8382-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="f8382-175">Изменения в модуле AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f8382-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="f8382-176">Новые командлеты для управления контекстом</span><span class="sxs-lookup"><span data-stu-id="f8382-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="f8382-177">[Enable-AzureRmContextAutosave][enable] — включение сохранения контекста для использования в разных сеансах PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f8382-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="f8382-178">Любые изменения влияют на глобальный контекст.</span><span class="sxs-lookup"><span data-stu-id="f8382-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="f8382-179">[Disable-AzureRmContextAutosave][disable] — отключение автосохранения контекста.</span><span class="sxs-lookup"><span data-stu-id="f8382-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="f8382-180">Для работы с новым сеансом PowerShell нужно будет выполнить вход.</span><span class="sxs-lookup"><span data-stu-id="f8382-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="f8382-181">[Select-AzureRmContext][select] — выбор контекста по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8382-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="f8382-182">Все последующие командлеты будут использовать для аутентификации учетные данные из этого контекста.</span><span class="sxs-lookup"><span data-stu-id="f8382-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="f8382-183">[Disconnect-AzureRmAccount][remove-cred] — удаление всех учетных данных и контекстов, связанных с учетной записью.</span><span class="sxs-lookup"><span data-stu-id="f8382-183">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="f8382-184">[Remove-AzureRmContext][remove-context] — удаление именованного контекста.</span><span class="sxs-lookup"><span data-stu-id="f8382-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="f8382-185">[Rename-AzureRmContext][rename] — переименование существующего контекста.</span><span class="sxs-lookup"><span data-stu-id="f8382-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="f8382-186">Изменения в существующих командлетах профиля</span><span class="sxs-lookup"><span data-stu-id="f8382-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="f8382-187">[Add-AzureRmAccount][login] — возможность входа на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8382-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="f8382-188">После входа разрешено присваивать имя контексту по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8382-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="f8382-189">[Import-AzureRmContext][import] — возможность входа на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8382-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="f8382-190">[Set-AzureRmContext][set-context] — возможность выбора существующих именованных контекстов и применения изменений на уровне процесса или текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="f8382-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
