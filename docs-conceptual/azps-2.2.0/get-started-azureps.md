---
title: Начало работы с Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 0c3b749cb2ac7f11dacafca76b65944f523f727d
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498160"
---
# <a name="get-started-with-azure-powershell"></a>Начало работы с Azure PowerShell

Среда Azure PowerShell оптимизирована для администрирования ресурсов Azure и управления ими из командной строки. С помощью Azure PowerShell можно создавать автоматизированные средства на основе модели Azure Resource Manager.
Попробуйте использовать его в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере.

В этой статье содержатся инструкции по началу работы с Azure PowerShell и объясняются основные принципы работы этой среды.

## <a name="install-or-run-in-azure-cloud-shell"></a>Установка или запуск в Azure Cloud Shell

Проще всего начать работу с Azure PowerShell в среде Azure Cloud Shell.
Чтобы скачать PowerShell и начать работу с Cloud Shell, см. [краткое руководство по использованию PowerShell в Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
Cloud Shell запускает PowerShell 6 в контейнере Linux, поэтому специальные функции Windows будут недоступны.

Когда все будет готово к установке Azure PowerShell на локальный компьютер, следуйте инструкциям, приведенным в статье [Install the Azure PowerShell module](install-az-ps.md) (Установка модуля Azure PowerShell).

## <a name="sign-in-to-azure"></a>Вход в Azure

Войдите в учетную запись в интерактивном режиме с помощью командлета `Connect-AzAccount`. При использовании Cloud Shell этот шаг можно пропустить: Сеанс Azure Cloud Shell уже прошел аутентификацию для среды, подписки и клиента, который запустил сеанс Cloud Shell.

```azurepowershell-interactive
Connect-AzAccount
```

Если вы находитесь за пределами США, используйте для входа параметр `-Environment`. Имя среды для вашего региона можно получить с помощью командлета [Get AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment). Например, для входа в учетную запись Azure China 21Vianet выполните следующую команду:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Вы получите токен, используемый на https://microsoft.com/devicelogin. Откройте эту страницу в браузере и введите токен, чтобы войти с данными учетной записи Azure и авторизовать Azure PowerShell. 

После входа вам отобразится информация о ваших активных подписках Azure. Если в вашей учетной записи есть несколько подписок Azure и вы хотите выбрать другую, получите список доступных подписок с помощью командлета [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) и выполните командлет [Set-AzContext](/powershell/module/az.accounts/set-azcontext) с указанием идентификатора своей подписки.
Дополнительные сведения об управлении подписками Azure в Azure PowerShell см. в статье [Use multiple Azure subscriptions](manage-subscriptions-azureps.md) (Использование нескольких подписок Azure).

После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для доступа и управления ресурсами в подписке. Дополнительные сведения о процессе входа и методах проверки подлинности см. в статье [Вход с помощью Azure PowerShell](authenticate-azureps.md).

## <a name="find-commands"></a>Поиск команд

В Azure PowerShell названия командлетов выбираются в соответствии со стандартным соглашением об именовании для PowerShell — `VERB-NOUN`. Глагол (часть verb) отвечает за действие (к ним относятся `Create`, `Get`, `Set`, `Delete`), а существительное (часть noun) — за тип ресурса (к ним относятся `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`). В Azure PowerShell существительное всегда начинается с префикса `Az`. Полный список стандартных глаголов см. в разделе [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Утвержденные глаголы для команд PowerShell).

Если вы знаете существительные и глаголы, с помощью модулей Azure PowerShell можно найти команды, выполнив командлет [Get-Command](/powershell/module/microsoft.powershell.core/get-command). Например, чтобы найти все связанные с виртуальной машиной команды, в которых используется глагол `Get` выполните следующий код:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Чтобы облегчить поиск часто используемых команд, в таблице ниже приведены типы ресурсов, указан соответствующий модуль Azure PowerShell и префикс для использования с командой `Get-Command`:

| Тип ресурса | модуль Azure PowerShell; | Префикс в существительном |
|---------------|-------------------------|----------------|
| [Группа ресурсов](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [Виртуальные машины](/azure/virtual-machines) | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [Учетные записи хранения](/azure/storage/common/storage-introduction) | [Az.Storage](/powershell/module/az.storage/) | `AzStorageAccount` |
| [хранилище ключей;](/azure/key-vault/key-vault-whatis) | [Az.KeyVault](/powershell/module/az.keyvault) | `AzKeyVault` |
| [Веб-приложения](/azure/app-service) | [Az.Websites](/powershell/module/az.websites) | `AzWebApp` |
| [Базы данных SQL](/azure/sql-database) | [Az.Sql](/powershell/module/az.sql) | `AzSqlDatabase` |

Полный список модулей для Azure PowerShell см. на [этой странице](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) сайта GitHub.

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Дополнительные сведения об основах работы с Azure PowerShell приведены в кратких руководствах и других материалах

Чтобы начать работу с Azure PowerShell, ознакомьтесь с подробным руководством по настройке виртуальных машин и отправке запросов на получение данных.

> [!div class="nextstepaction"]
> [Создание виртуальных машин с помощью Azure PowerShell](azureps-vm-tutorial.yml)

Кроме того, можно воспользоваться краткими руководствами по Azure PowerShell для других популярных служб Azure:

* [создать учетную запись хранения;](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Передача объектов в хранилище BLOB-объектов Azure и из него](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Создание и извлечение секретов из Azure Key Vault](/azure/key-vault/quick-create-powershell)
* [Создание базы данных Azure SQL и брандмауэра](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Запуск контейнеров в службе "Экземпляры контейнеров Azure"](/azure/container-instances/container-instances-quickstart-powershell)
* [Создание масштабируемого набора виртуальных машин (VMSS)](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Создание подсистемы балансировки нагрузки уровня "Стандартный"](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>Дополнительная информация

* [Вход с помощью Azure PowerShell](authenticate-azureps.md)
* [Управление подписками Azure с помощью Azure PowerShell](manage-subscriptions-azureps.md)
* [Создание субъектов-служб Azure с помощью Azure PowerShell](create-azure-service-principal-azureps.md)
* Помощь от сообщества:
  * [Форум Azure на MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](http://go.microsoft.com/fwlink/?LinkId=320213)
