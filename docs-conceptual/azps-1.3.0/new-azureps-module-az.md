---
title: Знакомство с модулем Az для Azure PowerShell
description: Знакомством с новым модулем Az для Azure PowerShell, который заменяет модуль AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: d08bca962b6ff65d25135150824b7c24fbd20103
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2019
ms.locfileid: "56145225"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Знакомство с новым модулем Az для Azure PowerShell

Начиная с декабря 2018 года модуль Az для Azure PowerShell есть в общедоступном выпуске и теперь является предполагаемым модулем PowerShell для работы с Azure. Модуль Az предлагает более короткие имена команд, улучшенную стабильность, а также кроссплатформенную поддержку. Az также обеспечивает равенство функций с модулем AzureRM и предлагает простой метод миграции со старого модуля.

Модуль Az использует библиотеку .NET Standard, благодаря чему он может работать в PowerShell 5.x и PowerShell 6.x.
PowerShell 6.x может запускаться на Linux, macOS и Windows, а это значит, что модуль Azure PowerShell доступен на всех платформах.
Использование .NET Standard позволяет унифицировать кодовую базу Azure PowerShell с минимальными последствиями для пользователей.

Az — это новый модуль, поэтому нумерация версий начинается с 1.0.0.

## <a name="upgrade-to-az"></a>Обновление до Az

Мы рекомендуем всем пользователям перейти на новый модуль Az. Для этого выполните следующие действия:

* __РЕКОМЕНДУЕТСЯ__: [Удалите модуль AzureRM для Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
* [Установите модуль Az для Azure PowerShell](/powershell/azure/install-az-ps).
* Активируйте режим совместимости, чтобы добавить псевдонимы для командлетов AzureRM с помощью `Enable-AzureRMAlias`, пока вы не ознакомитесь с новым набором команд. Включайте псевдонимы __только__ в том случае, если у вас не установлено AzureRM.

## <a name="migrate-existing-scripts-to-az"></a>Миграция существующих скриптов на Az

Значительные обновления могут быть сопряжены со сложностями. Однако в модуле Az предусмотрен режим совместимости, который позволяет использовать существующие скрипты, пока вы выполняете обновление для нового синтаксиса. Используйте командлет `Enable-AzureRmAlias` для активации режима совместимости AzureRM. Этот командлет определяет имена командлета AzureRM как псевдонимы для новых имен командлета Az.

Новые имена командлетов выбраны таким образом, чтобы их было легко запомнить. Вместо имен командлетов `AzureRm` или `Azure` используйте `Az`. Например, вместо старой команды `New-AzureRMVm` используется `New-AzVm`.

Полное описание процесса миграции см. в статье [Миграция с AzureRM на Az для Azure PowerShell](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Поддержка AzureRM в будущем

Существующий модуль AzureRM больше не будет получать новые командлеты или функции. Но AzureRM по-прежнему официально поддерживается и будет получать исправления ошибок до декабря 2020 г. Для поддержки новых служб и функций Azure перейдите на модуль Az.
