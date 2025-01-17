---
title: Знакомство с модулем Az для Azure PowerShell
description: Знакомством с новым модулем Az для Azure PowerShell, который заменяет модуль AzureRM.
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 21d41b6e14d1b39a78e40daee74b80de3a80c2a0
ms.sourcegitcommit: b02cbcd00748a4a9a4790a5fba229ce53c3bf973
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/09/2019
ms.locfileid: "68861299"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Знакомство с новым модулем Az для Azure PowerShell

Начиная с декабря 2018 года модуль Az для Azure PowerShell есть в общедоступном выпуске и теперь является предполагаемым модулем PowerShell для работы с Azure. Модуль Az предлагает более короткие имена команд, улучшенную стабильность, а также кроссплатформенную поддержку. Кроме того, для AZ реализовано равенство функций с AzureRM, что обеспечивает простоту перехода.

Благодаря модулю Az среда Azure PowerShell теперь совместима с PowerShell 5.1 в Windows и PowerShell Core 6.x и более поздней версии на всех поддерживаемых платформах, включая Windows, macOS и Linux.

Az — это новый модуль, поэтому нумерация версий начинается с 1.0.0.

## <a name="why-a-new-module"></a>Преимущества нового модуля

Значительные обновления могут быть сопряжены со сложностями, поэтому важно узнать, почему было принято решение представить новый набор модулей с новыми командлетами для взаимодействия с Azure через PowerShell.

Самое большое и важное изменение заключается в том, что PowerShell стал кроссплатформенным продуктом с момента появления [PowerShell Core 6.x](/powershell/scripting/overview) на основе библиотеки .NET Standard.
Мы стремимся обеспечить поддержку Azure на всех платформах. Это означает, что модули Azure PowerShell необходимо обновить для использования .NET Standard и совместимости с PowerShell Core. Вместо того чтобы вносить в существующий модуль AzureRM сложные изменения для добавления этой поддержки, был создан модуль Az.

Это решение также дало нашим инженерам возможность согласовать проектирование и именование командлетов и модулей. Все модули теперь начинаются с префикса `Az.`, а все командлеты используют форму _команда_-`Az`_существительное_. Ранее имена командлетов не только были длиннее, но и в них были несоответствия.

Количество модулей уменьшилось. Некоторые модули, которые работали с одинаковыми службами, были объединены, а командлеты плоскости управления и плоскости данных теперь содержатся в едином модуле для работы с соответствующими службами. Это упрощает задачу для тех, кто вручную управляет зависимостями и импортом.

Выполняя эти важные изменения, которые привели к созданию модуля Azure PowerShell, команда стремилась максимально упростить использование Azure с помощью командлетов PowerShell и добавить поддержку большего количества платформ, чем ранее.

## <a name="upgrade-to-az"></a>Обновление до Az

Для поддержки новых функций Azure в PowerShell необходимо как можно скорее перейти на модуль Az. Если вы не готовы установить модуль Az в качестве замены AzureRM, вам доступны несколько способов экспериментирования с Az.

* Использование среды `PowerShell` с [Azure Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview).
  Azure Cloud Shell — это браузерная среда оболочки, которая поставляется с пакетом установки модуля Az и поддерживает псевдонимы совместимости `Enable-AzureRM`.
* Оставив установленный модуль AzureRM с PowerShell 5.1 для Windows, установите модуль Az для PowerShell Core 6.x или более поздней версии. PowerShell 5.1 для Windows и PowerShell Core используют отдельные коллекции модулей. Следуйте инструкциям, чтобы [установить PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows), а затем [установите модуль Az](install-az-ps.md) из терминала PowerShell Core.

Чтобы выполнить обновление из существующей установки AzureRM, сделайте следующее:

1. [Удалите модуль AzureRM для Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
2. [Установите модуль Az для Azure PowerShell](install-az-ps.md).
3. __НЕОБЯЗАТЕЛЬНО__. Активируйте режим совместимости, чтобы добавить псевдонимы для командлетов AzureRM с помощью [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias), пока вы не ознакомитесь с новым набором команд. Дополнительные сведения см. в следующем разделе или в статье [Перенос Azure PowerShell с AzureRM на Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-to-az"></a>Миграция существующих скриптов на Az

Новые имена командлетов выбраны таким образом, чтобы их было легко запомнить. Вместо имен командлетов `AzureRm` или `Azure` используйте `Az`. Например, вместо старой команды `New-AzureRMVm` используется `New-AzVm`.
При переносе вам нужно не просто ознакомиться с новыми именами командлетов. Были переименованы модули, параметры и внесено много других важных изменений.

Чтобы упростить процесс перехода с AzureRM на Az, у нас есть ряд ресурсов:

* [Перенос Azure PowerShell с AzureRM на Az](migrate-from-azurerm-to-az.md)
* [Полный список критических изменений между AzureRM и Az 1.0.0](migrate-az-1.0.0.md)
* Командлет [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

В модуле Az предусмотрен режим совместимости, который позволяет использовать существующие скрипты, пока вы выполняете обновление для нового синтаксиса. Командлет [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) активирует режим совместимости через псевдонимы, чтобы можно было использовать существующие скрипты с минимальными изменениями во время подготовки к полному переходу на Az.

> [!IMPORTANT]
> Несмотря на то что для имен командлетов используются псевдонимы, все же могут существовать новые (или переименованные) параметры или измененные возвращаемые значения для командлетов Az. Не ожидайте, что активация псевдонимов обеспечит миграцию для вас. Ознакомьтесь с [полным списком критических изменений](migrate-az-1.0.0.md), чтобы узнать, где в скриптах могут потребоваться обновления.

## <a name="continued-support-for-azurerm"></a>Дальнейшая поддержка AzureRM

В AzureRM больше не будут добавляться новые командлеты или функции. Но модуль AzureRM по-прежнему официально поддерживается. В нем будут исправляться ошибки до декабря 2020 года.