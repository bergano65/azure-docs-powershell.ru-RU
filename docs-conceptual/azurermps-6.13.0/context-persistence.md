---
title: Использование учетных данных пользователя в разных сеансах PowerShell
description: Узнайте, как использовать учетные данные Azure и другие сведения в нескольких сеансах PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: 1e5c89a43886343bfc0a1affb5133a7cb6af0bcc
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "65854148"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a>Использование учетных данных пользователя в разных сеансах PowerShell

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

В Azure PowerShell существует функция **автосохранения контекста Azure**, которая предоставляет следующие возможности:

- хранение учетных данных для входа для повторного использования в новых сеансах PowerShell;
- упрощенное использование фоновых задач для запуска долго выполняющихся командлетов;
- переключение между учетными записями, подписками и средами без необходимости выполнять отдельный вход;
- одновременное выполнение задач с использованием разных учетных данных и подписок в рамках одного сеанса PowerShell.

## <a name="azure-contexts-defined"></a>Определенные контексты Azure

*Контекст Azure* — это набор сведений, которые определяют целевой объект для командлетов Azure PowerShell. Контекст состоит из пяти частей:

- *Учетная запись* — имя пользователя или субъекта-службы, которое используется для аутентификации при обмене данными со средой Azure.
- *Подписка* — подписка Azure с используемыми ресурсами.
- *Клиент* — клиент Azure Active Directory, который содержит вашу подписку. Клиенты являются более важными при аутентификации субъекта-службы.
- *Среда* — определяемое облако Azure (обычно это глобальное облако Azure).
  Кроме того, параметр среды позволяет определять национальные и локальные (Azure Stack) облака, а также облака для государственных организаций.
- *Учетные данные* — сведения, которые используются в Azure, чтобы выполнить идентификацию и авторизацию для доступа к ресурсам в Azure.

В предыдущих выпусках контекст Azure нужно было создавать при каждом открытии нового сеанса PowerShell. Начиная с версии Azure PowerShell 4.4.0, поддерживается автоматическое сохранение контекста Azure при каждом открытии нового сеанса PowerShell.

## <a name="automatically-save-the-context-for-the-next-sign-in"></a>Автоматическое сохранение контекста для следующего входа

Начиная с версии Azure PowerShell 6.3.0, данные контекста автоматически сохраняются между сеансами. Чтобы PowerShell не сохранял учетные данные и данные контекста, используйте `Disable-AzureRmContextAutoSave`. Для работы с новым сеансом PowerShell вам нужно будет войти в Azure.

Чтобы разрешить Azure PowerShell запоминать контекст после закрытия сеанса PowerShell, используйте `Enable-AzureRmContextAutosave`. Учетные данные и данные контекста автоматически сохраняются в специальной скрытой папке в каталоге пользователя (`%AppData%\Roaming\Windows Azure PowerShell`).
Каждый новый сеанс PowerShell обращается к контексту, который использовался в последнем сеансе.

Командлеты, которые помогают управлять контекстами Azure, также предоставляют удобные средства. С их помощью вы можете применить изменения как для текущего сеанса PowerShell (область `Process`), так и для всех сеансов PowerShell (область `CurrentUser`). Эти параметры будут подробно описаны в разделе [Использование областей контекстов](#using-context-scopes).

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a>Выполнение командлетов Azure PowerShell как фоновых заданий

Функция **автосохранения контекста Azure** также позволяет использовать контекст с фоновыми заданиями PowerShell. PowerShell позволяет запускать и отслеживать долго выполняющиеся задачи как фоновые задания. Для этого вам не нужно дожидаться завершения их выполнения. Чтобы использовать в фоновых заданиях учетные данные, можно сделать следующее:

- Передать контекст как аргумент.

  Большинство командлетов AzureRM позволяют передавать контекст как параметр. Передать контекст в фоновое задание можно так:

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- Использовать контекст по умолчанию со включенной функцией автосохранения

  Если включить функцию **автосохранения контекста**, фоновые задания будут автоматически использовать сохраненный контекст по умолчанию.

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

Если вам нужно узнать выходные данные фоновой задачи, используйте `Get-Job`, чтобы проверить состояние задания, и `Wait-Job`, чтобы дождаться завершения задания. Используйте `Receive-Job`, чтобы записать или отобразить выходные данные фонового задания. См. дополнительные сведения о [заданиях](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="creating-selecting-renaming-and-removing-contexts"></a>Создание, выбор, переименование и удаление контекстов

Чтобы создать контекст, нужно войти в Azure. Командлет `Connect-AzureRmAccount` (или его псевдоним `Login-AzureRmAccount`) определяет контекст по умолчанию, который будет использоваться командлетами Azure PowerShell. Он также обеспечивает доступ к любому клиенту или подписке в рамках разрешений, предоставляемых вашими учетными данными.

Чтобы добавить новый контекст после входа, используйте командлет `Set-AzureRmContext` (или его псевдоним `Select-AzureRmSubscription`).

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

В примере выше мы добавили новый контекст для подписки "Contoso Subscription 1", используя текущие учетные данные. Новый контекст называется "Contoso1". Если вы не укажете имя для контекста, будет использоваться имя по умолчанию на основе идентификатора учетной записи и подписки.

Чтобы переименовать существующий контекста, используйте командлет `Rename-AzureRmContext`. Например:

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

В этом примере мы изменяем стандартное имя контекста `[user1@contoso.org; 123456-7890-1234-564321]` на простое имя "Contoso2". Командлеты, которые управляют контекстами, также поддерживают заполнение нажатием клавиши TAB. Это позволяет быстро выбрать контекст.

Наконец, чтобы удалить контекст, используйте командлет `Remove-AzureRmContext`.  Например:

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

Удаление контекста с именем "Contoso2". Этот контекст можно создать повторно с помощью командлета `Set-AzureRmContext`.

## <a name="removing-credentials"></a>Удаление учетных данных

Вы можете удалить все учетные данные и связанные контексты пользователя или субъекта-службы с помощью командлета `Disconnect-AzureRmAccount` (или его псевдонима `Logout-AzureRmAccount`). Выполняемый без параметров командлет `Disconnect-AzureRmAccount` удаляет все учетные данные и контексты, связанные с пользователем или субъектом-службой в текущем контексте. Чтобы связать с контекстом определенный субъект, вы можете передать имя пользователя, имя субъекта-службы или сам контекст.

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a>Использование областей контекстов

Иногда нужно выбрать, изменить или удалить контекст в сеансе PowerShell, не влияя на другие сеансы. Чтобы изменить стандартное поведение командлетов, управляющих контекстом, используйте параметр `Scope`. Область `Process` переопределяет стандартное поведение, ограничивая его действие текущим сеансом. И наоборот, область `CurrentUser` изменяет контекст во всех сеансах, а не только в текущем.

Например, вот как можно изменить контекст по умолчанию в текущем сеансе PowerShell, не влияя на другие окна, или изменить контекст, который будет использоваться при следующем открытии сеанса:

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a>Запоминание параметра автосохранения контекста

Параметр автосохранения контекста сохраняется в каталоге пользователя Azure PowerShell (`%AppData%\Roaming\Windows Azure PowerShell`). На некоторых компьютерах учетные записи могут не иметь доступ к этому каталогу. В таких случаях можно использовать переменную среды

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

Если задано значение true, контекст сохраняется автоматически. Если задано значение false, контекст не сохраняется.

## <a name="changes-to-the-azurermprofile-module"></a>Изменения в модуле AzureRM.Profile

Новые командлеты для управления контекстом

- [Enable-AzureRmContextAutosave][enable] — включение сохранения контекста для использования в разных сеансах PowerShell.
  Любые изменения влияют на глобальный контекст.
- [Disable-AzureRmContextAutosave][disable] — отключение автосохранения контекста. Для работы с новым сеансом PowerShell нужно будет выполнить вход.
- [Select-AzureRmContext][select] — выбор контекста по умолчанию. Все командлеты используют для аутентификации учетные данные из этого контекста.
- [Disconnect-AzureRmAccount][remove-cred] — удаление всех учетных данных и контекстов, связанных с учетной записью.
- [Remove-AzureRmContext][remove-context] — удаление именованного контекста.
- [Rename-AzureRmContext][rename] — переименование существующего контекста.

Изменения в существующих командлетах профиля

- [Add-AzureRmAccount][login] — возможность входа на уровне процесса или текущего пользователя.
  После аутентификации разрешено присваивать имя контексту по умолчанию.
- [Import-AzureRmContext][import] — возможность входа на уровне процесса или текущего пользователя.
- [Set-AzureRmContext][set-context] — возможность выбора существующих именованных контекстов и применения изменений на уровне процесса или текущего пользователя.

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext
