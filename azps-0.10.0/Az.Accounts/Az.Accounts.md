---
Module Name: Az.Accounts
Module Guid: 342714fc-4009-4863-8afb-a9067e3db04b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.accounts
Help Version: 4.6.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Az.Accounts.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Az.Accounts.md
ms.openlocfilehash: c0f8ea29a795b7b88a6e79134d52c3dd00ad5f42
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909282"
---
# AZ. Accounts
## Nописание
Управление учетными данными и общей конфигурацией для всех модулей Azure.

## Командлеты AZ. Accounts
### [Add-AzEnvironment](Add-AzEnvironment.md)
Добавляет конечные точки и метаданные для экземпляра диспетчера ресурсов Azure.

### [Clear-AzContext](Clear-AzContext.md)
Удалите все учетные данные Azure, учетную запись и сведения о подписке.

### [Clear-AzDefault](Clear-AzDefault.md)
Очищает значения по умолчанию, заданные пользователем в текущем контексте.

### [Connect-AzAccount](Connect-AzAccount.md)
Подключитесь к Azure с учетной записью, прошедшим проверку подлинности, для использования с запросом командлетов Azure Resource Manager.

### [Disable-AzContextAutosave](Disable-AzContextAutosave.md)
Отключите Автосохранение учетных данных Azure.  Ваши регистрационные данные будут утрачены при следующем открытии окна PowerShell.

### [Disable-AzDataCollection](Disable-AzDataCollection.md)
Изменяют сбор данных, чтобы улучшить командлеты AzurePowerShell. Данные не собираются, пока не будет явно задействовано.

### [Disable-AzureRmAlias](Disable-AzureRmAlias.md)
Отключает псевдонимы префиксов AzureRm для модулей AZ.

### [Разъединить — AzAccount](Disconnect-AzAccount.md)
Отключение подключенной учетной записи Azure и удаление всех учетных данных и контекстов, связанных с этой учетной записью.

### [Enable-AzContextAutosave](Enable-AzContextAutosave.md)
Предоставление учетных данных Azure, учетной записи и сведений о подписке для сохранения и автоматической загрузки при открытии окна PowerShell. 

### [Enable-AzDataCollection](Enable-AzDataCollection.md)
Позволяет Azure PowerShell собирать данные, чтобы улучшить взаимодействие с пользователем с помощью командлетов AzurePowerShell.
Выполнение этого командлета наследуется в сборе данных для текущего пользователя на текущем компьютере.
Никакие данные не собираются, пока не будет явно задействовано.

### [Enable-AzureRmAlias](Enable-AzureRmAlias.md)
Включает псевдонимы префиксов AzureRm для модулей AZ.

### [Get-AzContext](Get-AzContext.md)
Получает метаданные, используемые для проверки подлинности запросов диспетчера ресурсов Azure.

### [Get-AzContextAutosaveSetting](Get-AzContextAutosaveSetting.md)
Отображение метаданных о функции автосохранения контекста, в том числе о том, сохраняется ли контекст автоматически, а также о том, где можно найти сохраненные сведения о контексте и учетных данных.

### [Get-AzDefault](Get-AzDefault.md)
Получение значений по умолчанию, заданных пользователем в текущем контексте.

### [Get-AzEnvironment](Get-AzEnvironment.md)
Получение конечных точек и метаданных для экземпляра служб Azure.

### [Get-AzProfile](Get-AzProfile.md)
Получение профилей служб, поддерживаемых установленными модулями.

### [Get-AzSubscription](Get-AzSubscription.md)
Получение подписок, доступ к которым разрешен текущей учетной записью.

### [Get-AzTenant](Get-AzTenant.md)
Возвращает клиентов, которые авторизованы для текущего пользователя.

### [Import-AzContext](Import-AzContext.md)
Загрузка данных проверки подлинности Azure из файла.

### [Регистрация — AzModule](Register-AzModule.md)
ДЛЯ внутренних целей — предоставление поддержки среды выполнения для командлетов, созданных с помощью автоотдыха

### [Remove-AzContext](Remove-AzContext.md)
Удаление контекста из набора доступных контекстов

### [Remove-AzEnvironment](Remove-AzEnvironment.md)
Удаляет конечные точки и метаданные для подключения к определенному экземпляру Azure.

### [Rename-AzContext](Rename-AzContext.md)
Переименуйте контекст Azure.  По умолчанию контексты названы учетной записью пользователя и подпиской.

### [Resolve-AzError](Resolve-AzError.md)
Отображение подробных сведений об ошибках PowerShell с дополнительными сведениями об ошибках Azure PowerShell.

### [Сохранить — AzContext](Save-AzContext.md)
Сохранение текущих сведений для проверки подлинности для использования в других сеансах PowerShell.

### [SELECT-AzContext](Select-AzContext.md)
Выбор подписки и учетной записи для назначения в командлетах PowerShell для Azure

### [SELECT-AzProfile](Select-AzProfile.md)
Для модулей, поддерживающих несколько профилей служб, загрузите командлеты, соответствующие заданному профилю службы.

### [Отправка и отзыв](Send-Feedback.md)
Отправляет отзыв команде Azure PowerShell с помощью набора интерактивных запросов.

### [Set-AzContext](Set-AzContext.md)
Задает клиента, подписку и среду для командлетов, используемых в текущем сеансе.

### [Set-AzDefault](Set-AzDefault.md)
Задает значение по умолчанию в текущем контексте.

### [Set-AzEnvironment](Set-AzEnvironment.md)
Задает свойства среды Azure.

### [Uninstall-AzureRm](Uninstall-AzureRm.md)
Удаление всех AzureRmных модулей с компьютера.

