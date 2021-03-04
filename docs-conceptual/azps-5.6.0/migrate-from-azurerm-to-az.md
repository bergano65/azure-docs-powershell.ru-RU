---
title: Перенос скриптов Azure PowerShell с AzureRM на Az
description: Узнайте о действиях и инструментах для переноса скриптов Azure PowerShell с модуля AzureRM на новый модуль Az PowerShell.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/15/2020
ms.custom: devx-track-azurepowershell, contperf-fy21q2
ms.openlocfilehash: 6bccaf9a628f67b8945516bae70f07939cdce8f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872524"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Перенос Azure PowerShell с AzureRM на Az

Все версии модуля AzureRM PowerShell устарели. [Модуль Az PowerShell](install-az-ps.md) теперь является рекомендуемым модулем PowerShell для взаимодействия с Azure.

## <a name="why-a-new-module"></a>Преимущества нового модуля

Самое большое и важное изменение заключается в том, что [PowerShell](/powershell/scripting/overview) является кросс-платформенным продуктом на основе библиотеки .NET Standard с момента своего появления.

Как и в случае с PowerShell, мы стремимся обеспечить поддержку Azure на всех платформах. Поэтому мы обновили модули Azure PowerShell для обеспечения совместимости с .NET Standard и PowerShell Core. Вместо того чтобы вносить в существующий модуль AzureRM сложные изменения для включения этой поддержки, был создан модуль Az.

Это решение также позволило нашим инженерам сделать разработку, модули и имена командлетов согласованными. Все модули теперь начинаются с префикса `Az.`, а все командлеты следуют соглашению об именовании, определяющем формат `Verb-AzNoun`. Раньше имена командлетов были длинными и непоследовательными.

Количество модулей также уменьшилось — некоторые модули, предназначенные для одних и тех же служб, были объединены. Командлеты плоскости управления и плоскости данных для одной службы теперь содержатся в отдельном модуле. Это упрощает задачу для тех, кто вручную управляет зависимостями и импортом.

Выполняя эти важные изменения, команда стремилась максимально упростить использование Azure с помощью командлетов PowerShell и добавить поддержку большего количества платформ, чем это было возможно ранее.

## <a name="upgrading-to-az-powershell"></a>Обновление до Az PowerShell

Скрипты, написанные для командлетов AzureRM, не смогут автоматически работать с Az. Чтобы упростить этот переход, был разработан [набор средств для миграции с AzureRM на Az](https://github.com/Azure/azure-powershell-migration). Миграция всегда сопряжена со сложностями, и эта статья поможет вам начать переход на новый модуль Az PowerShell. Дополнительные сведения о том, для чего был создан модуль Az PowerShell, см. в статье [Знакомство с новым модулем Az для Azure PowerShell](new-azureps-module-az.md).

Новые имена командлетов выбраны таким образом, чтобы их было легко запомнить. Вместо имен командлетов `AzureRm` или `Azure` используйте `Az`. Например, вместо старого командлета `New-AzureRMVm` используется `New-AzVm`.
Но при переносе вам нужно не просто ознакомиться с новыми именами командлетов. Были переименованы модули, параметры и внесено много других важных изменений.

Полный список критических изменений между AzureRM и Az см. [здесь](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Убедитесь, что существующие скрипты работают с последним выпуском AzureRM

Перед выполнением любых действий миграции проверьте, какие версии AzureRM установлены в вашей системе.
Так вы проверите, запущены ли скрипты с последним выпуском, и узнаете, какие версии AzureRM необходимо удалить.

Чтобы проверить установленные версии AzureRM, выполните приведенный ниже пример.

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

**Последний** доступный выпуск AzureRM — **6.13.1**. Если у вас нет этой версии, возможно, ваши существующие скрипты нужно будет изменить для работы с модулем Az наряду с изменениями, описанными в этой статье и [списке критических изменений](migrate-az-1.0.0.md).

Если скрипты не работают с AzureRM 6.13.1, обновите их в соответствии с [руководством по переходу AzureRM с версии 5.x на 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Если вы используете более раннюю версию модуля AzureRM, найдите нужное руководство. Руководства по миграции существуют для каждого основного номера версии.

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>Вариант 1 (рекомендуется). Автоматический перенос скриптов PowerShell

Этот рекомендуемый вариант предполагает минимум усилий с вашей стороны для переноса скриптов AzureRM в Az.

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>Установка набора средств для миграции с AzureRM на Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>Автоматическое преобразование скриптов

Используя набор средств для миграции с AzureRM на Az, вы можете подготовить план, который определяет изменения, которые будут внесены в скрипты до их внесения и установки модуля Az PowerShell.

В статье [Краткое руководство. Автоматическая миграция скриптов PowerShell из AzureRM в модуль Az PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) показано, как выполнить автоматический перенос скриптов PowerShell из AzureRM в модуль Az PowerShell.

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>Вариант 2. Использование режима совместимости с помощью Enable-AzureRmAlias

В модуле Az предусмотрен режим совместимости, который позволяет использовать существующие скрипты, пока вы выполняете обновление для нового синтаксиса. Командлет [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) включает режим совместимости с использованием псевдонимов. Так вы сможете использовать существующие скрипты с минимальными изменениями во время подготовки к полному переходу на Az. По умолчанию `Enable-AzureRmAlias` включает псевдонимы совместимости только для текущего сеанса PowerShell. Используйте его параметр `Scope`, чтобы псевдонимы совместимости поддерживались во всех сеансах PowerShell. Дополнительные сведения см. в справочной статье о командлете [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Несмотря на то что для имен командлетов используются псевдонимы, все же могут существовать новые (или переименованные) параметры или измененные возвращаемые значения для командлетов Az. Не ожидайте, что активация псевдонимов обеспечит миграцию для вас. Ознакомьтесь с [полным списком критических изменений](migrate-az-1.0.0.md), чтобы узнать, где в скриптах могут потребоваться обновления.

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>Способ 3. Перенос скриптов в Visual Studio Code с помощью расширения Azure PowerShell

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>Установка расширения Azure PowerShell для Visual Studio Code

Установите [расширение Azure PowerShell для VS Code](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools).

### <a name="convert-your-scripts-manually"></a>Преобразование скриптов вручную

1. Загрузите скрипт AzureRM в VS Code.
2. Начните миграцию, открыв палитру команд с помощью клавиш `Ctrl+Shift+P` и выбрав `Migrate Azure PowerShell script`.
3. Выберите исходную версию `AzureRM`.
4. Выполните рекомендуемые действия для каждой команды или параметра.

## <a name="next-steps"></a>Дальнейшие действия

* [Удаление AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
* [Установка Azure PowerShell](install-az-ps.md)
