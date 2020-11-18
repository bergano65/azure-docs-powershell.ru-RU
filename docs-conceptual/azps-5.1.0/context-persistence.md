---
title: Контексты Azure и учетные данные для входа
description: Узнайте, как использовать учетные данные Azure и другие сведения в нескольких сеансах PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: be9113ab1ad6a359832634ae2c21fd177b09318f
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715600"
---
# <a name="azure-powershell-context-objects"></a>Объекты контекста Azure PowerShell

Azure PowerShell использует _объекты контекста Azure PowerShell_ (контексты Azure) для хранения информации о подписке и аутентификации. При наличие нескольких подписок, контексты Azure позволяют выбрать подписку для запуска командлетов Azure PowerShell. Контексты Azure также используются для хранения данных для входа в несколько сеансов PowerShell и выполнения фоновых задач.

Эта статья посвящена рассмотрению управления контекстами Azure, а не подписками или учетными записями. Если вы хотите управлять пользователями, подписками, клиентами или другой информацией об учетной записи, см. документацию по [Azure Active Directory](/azure/active-directory). Чтобы узнать, как использовать контексты для выполнения фоновых или параллельных задач, см. раздел [Выполнение командлетов в параллельном режиме с помощью заданий PowerShell](using-psjobs.md) после ознакомления с контекстами Azure.

## <a name="overview-of-azure-context-objects"></a>Обзор объектов контекста Azure

Контексты Azure — это объекты PowerShell, которые представляют активную подписку для выполнения команд и информацию об аутентификации, необходимую для подключения к облаку Azure. Благодаря контекстам Azure, Azure PowerShell не требуется повторная аутентификация учетной записи при каждом переключении между подписками. Контекст Azure состоит из:

* _Учетной записи_, использованной для входа в Azure с помощью [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount). Контексты Azure обрабатывают пользователей, идентификаторы приложения и субъект-службы одинаково с точки зрения учетной записи.
* Активной _подписки_, соглашения об обслуживании Майкрософт для создания и запуска ресурсов Azure, связанных с _клиентом_. В документации или при работе с Active Directory клиентов часто называют _организациями_.
* Ссылка на _кэш токена_ — сохраненный токен аутентификации для доступа к облаку Azure. [Настройки автосохранения контекста](#save-azure-contexts-across-powershell-sessions) определяют место и срок хранения этого токена.

Дополнительные сведения об этих условиях см. в разделе [Терминология Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology). Токены аутентификации, используемые контекстами Azure, подобны другим сохраненным токенам, являющимся частью постоянного сеанса.

При входе с помощью `Connect-AzAccount`для подписки по умолчанию создается как минимум один контекст Azure. Объект, возвращаемый `Connect-AzAccount` является контекстом Azure по умолчанию, используемым до конца сеанса PowerShell.

## <a name="get-azure-contexts"></a>Получение контекстов Azure

Доступные контексты Azure извлекаются с помощью командлета [Get-AzContext](/powershell/module/az.accounts/get-azcontext). Перечислите все доступные контексты с помощью `-ListAvailable`:

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

Или получите контекст по имени:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

Имена контекстов могут отличаться от имен связанных подписок.

> [!IMPORTANT]
> Доступные контексты Azure __не__ всегда являются доступными подписками. Контексты Azure представляют только локально хранимую информацию. Вы можете получить подписки с помощью командлета [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription).

## <a name="create-a-new-azure-context-from-subscription-information"></a>Создание нового контекста Azure из сведений о подписке

Командлет [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) используется как для создания новых контекстов Azure, так и для их установки в качестве активного контекста.
Самый простой способ создать новый контекст Azure — использовать существующие сведения о подписке. Командлет предназначен для получения объекта вывода из `Get-AzSubscription` в качестве переданного значения и настройки нового контекста Azure:

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

При необходимости укажите либо имя, либо идентификатор подписки и идентификатор клиента:

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

Если аргумент `-Name` пропущен, имя и идентификатор подписки используются в качестве имени контекста в формате `Subscription Name (subscription-id)`.

## <a name="change-the-active-azure-context"></a>Изменение активного контекста Azure

Для изменения активного контекста Azure можно использовать как `Set-AzContext`, так и [Select-AzContext](/powershell/module/az.accounts/set-azcontext). Как описано в статье [Создание нового контекста Azure](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` создает новый контекст Azure для подписки, если он не существует, а затем переключается на использование этого контекста в качестве активного.

`Select-AzContext` предназначен для использования только с существующими контекстами Azure и работает аналогично использованию `Set-AzContext -Context`, но предназначен для использования с конвейером:

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

Как и многие другие команды управления учетными записями и контекстами в Azure PowerShell, `Set-AzContext` и `Select-AzContext` поддерживают аргумент `-Scope`, чтобы можно было контролировать продолжительность активного контекста. `-Scope` позволяет изменить активный контекст одного сеанса, не меняя значение по умолчанию:

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

Чтобы избежать переключения контекстов для всего сеанса PowerShell, все команды Azure PowerShell могут выполняться в данном контексте с аргументом `-AzContext`:

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

Другое основное использование контекстов с командлетами Azure PowerShell — запуск фоновых команд. Дополнительные сведения о запуске заданий PowerShell с помощью Azure PowerShell см. в разделе [Выполнение командлетов PowerShell Azure в заданиях PowerShell](using-psjobs.md).

## <a name="save-azure-contexts-across-powershell-sessions"></a>Сохранение контекстов Azure в сеансах PowerShell

По умолчанию контексты Azure сохраняются для использования между сеансами PowerShell. Это поведение можно изменить следующими способами:

* Войдите, используя `-Scope Process` с помощью `Connect-AzAccount`.

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  Контекст Azure, возвращенный как часть этого входа, действителен _только_ для текущего сеанса и не будет автоматически сохраняться независимо от параметра автосохранения контекста Azure PowerShell.
* Отключите автосохранение контекста Azure Powershell с помощью командлета [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).
  Отключение автосохранения контекста __не__ удаляет сохраненные токены. Чтобы узнать, как очистить сохраненную информацию о контексте Azure, см. раздел [Удаление контекстов и учетных данных Azure](#remove-azure-contexts-and-stored-credentials).
* Явное включение автосохранения контекста Azure можно включить с помощью командлета [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave). При включенном автосохранении все контексты пользователя хранятся локально для последующих сеансов PowerShell.
* Сохраните контексты вручную с помощью [Save-AzContext](/powershell/module/az.accounts/save-azcontext) для использования в будущих сеансах PowerShell, где их можно загрузить с помощью командлета [Import-AzContext](/powershell/module/az.accounts/import-azcontext):

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> Отключение автосохранения контекста __не__ удаляет сохраненную информацию контекста. Чтобы удалить сохраненную информацию, используйте командлет [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Подробнее об удалении сохраненных контекстов см. раздел [Удаление контекстов и учетных данных](#remove-azure-contexts-and-stored-credentials).

Каждая из этих команд поддерживает параметр `-Scope`, который может принимать значение `Process` только для текущего запущенного процесса. Например, чтобы убедиться, что вновь созданные контексты не сохраняются после выхода из сеанса PowerShell:

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

Информация контекстов и токены хранятся в каталоге `$env:USERPROFILE\.Azure` в Windows и в `$HOME/.Azure` — на других платформах. Конфиденциальная информация, такая как идентификаторы подписки и идентификаторы клиентов, может по-прежнему отображаться в сохраненной информации через журналы или сохраненные контексты. Чтобы узнать, как очистить сохраненную информацию, см. раздел [Удаление контекстов и учетных данных](#remove-azure-contexts-and-stored-credentials).

## <a name="remove-azure-contexts-and-stored-credentials"></a>Удаление контекстов Azure и сохраненных учетных данных

Для удаления контекстов и учетных данных Azure выполните следующие действия:

* Выйдите из учетной записи с помощью командлета [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).
  Используя учетную запись или контекст, можно выйти из любой учетной записи.

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  При отключении всегда удаляются сохраненные токены аутентификации и очищаются сохраненные контексты, связанные с отключенным пользователем или контекстом.
* Используйте [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext). Этот командлет гарантированно всегда удаляет сохраненные контексты и токены аутентификации, а также выводит вас из системы.
* Удаление контекста с помощью [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):

  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  При удалении активного контекста, вы будете отключены от Azure. Вам также потребуется повторно выполнить проверку подлинности с помощью `Connect-AzAccount`.

## <a name="see-also"></a>См. также раздел

* [Запуск командлетов Azure PowerShell в заданиях PowerShell](using-psjobs.md)
* [Терминология Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [Справочные материалы по Az.Accounts](/powershell/module/az.accounts)
