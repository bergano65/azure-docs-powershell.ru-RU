---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: 0c8773066f39d11e6985bbe4bd1f1e69cd9142f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990632"
---
# Модуль Az.Accounts
## Описание
Управление учетными данными и общей конфигурацией для всех модулей Azure.

## Az.Accounts Cmdlets
### [Add-AzEnvironment](Add-AzEnvironment.md)
Добавляет конечные точки и метаданные для экземпляра Azure Resource Manager.

### [Clear-AzContext](Clear-AzContext.md)
Удалите все учетные данные Azure, учетную запись и данные подписки.

### [Clear-AzDefault](Clear-AzDefault.md)
Очищает значения по умолчанию, установленные пользователем в текущем контексте.

### [Connect-AzAccount](Connect-AzAccount.md)
Подключайтесь к Azure с помощью учетной записи, авторизированной для использования с командлетами из модулей Az PowerShell.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Отключите автосбереги учетных данных Azure.  При следующем входе в окно PowerShell ваши данные будут забыты

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Отказ от сбора данных для улучшения работы с azure PowerShell. Данные собираются по умолчанию, если вы явным образом не откажетлись от них.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Отключает псевдонимы префиксов AzureRm для модулей Az.

### [Disconnect-AzAccount](Disconnect-AzAccount.md)
Отключает подключенную учетную запись Azure и удаляет все учетные данные и контексты, связанные с ней.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
Контексты Azure — это объекты PowerShell, представляющие активную подписку для запуска команд, а также сведения о проверке подлинности, необходимые для подключения к облаку Azure. В контекстах Azure Azure PowerShell не нужно повторно реакторировать вашу учетную запись при смене подписки. Дополнительные сведения см. в [контекстных объектах Azure PowerShell.](https://docs.microsoft.com/powershell/azure/context-persistence)

Этот cmdlet позволяет сохранить контекстные данные Azure и автоматически загружать их при запуске powerShell. Например, при открытии нового окна.

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Позволяет Azure PowerShell собирать данные для улучшения пользовательского интерфейса с помощью cmdlets Azure PowerShell. При выполнении этого cmdlet выполняется сбор данных текущего пользователя на текущем компьютере. Данные собираются по умолчанию, если вы явным образом не откажетлись от них.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Включает псевдонимы префиксов AzureRm для модулей Az.

### [Get-AzAccessToken](Get-AzAccessToken.md)
Получить необработанные маркеры доступа. При использовании ресурса ResourceUrl убедитесь, что значение соответствует текущей среде Azure. Вы можете ссылаться на значение `(Get-AzContext).Environment` .

### [Get-AzContext](Get-AzContext.md)
Возвращает метаданные, используемые для проверки подлинности запросов Диспетчера ресурсов Azure.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
Отображение метаданных о функции автосбобоя контекста, в том числе о том, будет ли автоматически сохранен контекст и где находятся сохраненные сведения о контексте и учетных данных.

### [Get-AzDefault](Get-AzDefault.md)
Установите значения по умолчанию для пользователя в текущем контексте.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Получите конечные точки и метаданные для экземпляра служб Azure.

### [Get-AzSubscription](Get-AzSubscription.md)
Получите подписки, к которые может получить доступ текущая учетная запись.

### [Get-AzTenant](Get-AzTenant.md)
Клиенты, авторизованные для текущего пользователя.

### [Import-AzContext](Import-AzContext.md)
Загружает данные проверки подлинности Azure из файла.

### [Invoke-AzRestMethod](Invoke-AzRestMethod.md)
Создание и выполнение HTTP-запроса только для конечной точки управления ресурсами Azure

### [Register-AzModule](Register-AzModule.md)
ТОЛЬКО ДЛЯ ВНУТРЕННЕГО ИСПОЛЬЗОВАНИЯ: поддержка runtime для автоматически созданных cmdlets

### [Remove-AzContext](Remove-AzContext.md)
Удаление контекста из набора доступных контекстов

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
Удаляет конечные точки и метаданные для подключения к экземпляру Azure.

### [Rename-AzContext](Rename-AzContext.md)
Переименуем контекст Azure.  По умолчанию контексты называются учетной записью пользователя и подпиской.

### [Resolve-AzError](Resolve-AzError.md)
Отображение подробных сведений об ошибках PowerShell и подробных сведений об ошибках Azure PowerShell.

### [Save-AzContext](Save-AzContext.md)
Сохранение текущих сведений проверки подлинности для использования в других сеансах PowerShell.

### [Select-AzContext](Select-AzContext.md)
Выбор подписки и учетной записи для целевой аудитории в azure PowerShell

### [Отправка отзыва](Send-Feedback.md)
Отправляет отзыв команде Azure PowerShell с помощью набора управляемых подсказок.

### [Set-AzContext](Set-AzContext.md)
Настраивает клиент, подписку и среду для использования в текущем сеансе.

### [Set-AzDefault](Set-AzDefault.md)
Задает значение по умолчанию в текущем контексте.

### [Set-AzEnvironment](Set-AzEnvironment.md)
Задает свойства среды Azure.

### [Удалить-AzureRm](Uninstall-AzureRm.md)
Удаляет все модули AzureRm с компьютера.

