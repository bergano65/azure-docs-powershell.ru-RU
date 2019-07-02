---
title: Начало работы с Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: c60036ba8be6282007aa34a0bb9c0d9e33197072
ms.sourcegitcommit: a4e527d3deba004007cfa22fa536e8255dd23b37
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2019
ms.locfileid: "67516816"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="69fae-102">Начало работы с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="69fae-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="69fae-103">Среда Azure PowerShell оптимизирована для администрирования ресурсов Azure и управления ими из командной строки.</span><span class="sxs-lookup"><span data-stu-id="69fae-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="69fae-104">С помощью Azure PowerShell можно создавать автоматизированные средства на основе модели Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="69fae-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="69fae-105">Попробуйте использовать его в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="69fae-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="69fae-106">В этой статье содержатся инструкции по началу работы с Azure PowerShell и объясняются основные принципы работы этой среды.</span><span class="sxs-lookup"><span data-stu-id="69fae-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="69fae-107">Установка или запуск в Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="69fae-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="69fae-108">Проще всего начать работу с Azure PowerShell в среде Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="69fae-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="69fae-109">Чтобы скачать PowerShell и начать работу с Cloud Shell, см. [краткое руководство по использованию PowerShell в Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="69fae-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="69fae-110">Cloud Shell запускает PowerShell 6 в контейнере Linux, поэтому специальные функции Windows будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="69fae-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="69fae-111">Когда все будет готово к установке Azure PowerShell на локальный компьютер, следуйте инструкциям, приведенным в статье [Install the Azure PowerShell module](install-az-ps.md) (Установка модуля Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="69fae-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="69fae-112">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="69fae-112">Sign in to Azure</span></span>

<span data-ttu-id="69fae-113">Войдите в учетную запись в интерактивном режиме с помощью командлета `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="69fae-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="69fae-114">При использовании Cloud Shell этот шаг можно пропустить: Сеанс Azure Cloud Shell уже прошел аутентификацию для среды, подписки и клиента, который запустил сеанс Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="69fae-114">Skip this step if you use Cloud Shell: Your Azure Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="69fae-115">Если вы находитесь за пределами США, используйте для входа параметр `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="69fae-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="69fae-116">Имя среды для вашего региона можно получить с помощью командлета [Get AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="69fae-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="69fae-117">Например, для входа в учетную запись Azure China 21Vianet выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="69fae-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="69fae-118">Вы получите токен, используемый на https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="69fae-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="69fae-119">Откройте эту страницу в браузере и введите токен, чтобы войти с данными учетной записи Azure и авторизовать Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="69fae-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="69fae-120">После входа вам отобразится информация о ваших активных подписках Azure.</span><span class="sxs-lookup"><span data-stu-id="69fae-120">After signing in, you'll see information indicating which of your Azure subscriptions is active.</span></span> <span data-ttu-id="69fae-121">Если в вашей учетной записи есть несколько подписок Azure и вы хотите выбрать другую, получите список доступных подписок с помощью командлета [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) и выполните командлет [Set-AzContext](/powershell/module/az.accounts/set-azcontext) с указанием идентификатора своей подписки.</span><span class="sxs-lookup"><span data-stu-id="69fae-121">If you have multiple Azure subscriptions in your account and want to select a different one, get your available subscriptions with [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) and use the [Set-AzContext](/powershell/module/az.accounts/set-azcontext) cmdlet with your subscription ID.</span></span>
<span data-ttu-id="69fae-122">Дополнительные сведения об управлении подписками Azure в Azure PowerShell см. в статье [Use multiple Azure subscriptions](manage-subscriptions-azureps.md) (Использование нескольких подписок Azure).</span><span class="sxs-lookup"><span data-stu-id="69fae-122">For more information about managing your Azure subscriptions in Azure PowerShell, see [Use multiple Azure subscriptions](manage-subscriptions-azureps.md).</span></span>

<span data-ttu-id="69fae-123">После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для доступа и управления ресурсами в подписке.</span><span class="sxs-lookup"><span data-stu-id="69fae-123">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="69fae-124">Дополнительные сведения о процессе входа и методах проверки подлинности см. в статье [Вход с помощью Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="69fae-124">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="69fae-125">Поиск команд</span><span class="sxs-lookup"><span data-stu-id="69fae-125">Find commands</span></span>

<span data-ttu-id="69fae-126">В Azure PowerShell названия командлетов выбираются в соответствии со стандартным соглашением об именовании для PowerShell — `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="69fae-126">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="69fae-127">Глагол (часть verb) отвечает за действие (к ним относятся `New`, `Get`, `Set`, `Remove`), а существительное (часть noun) — за тип ресурса (к ним относятся `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="69fae-127">The verb describes the action (examples include `New`, `Get`, `Set`, `Remove`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="69fae-128">В Azure PowerShell существительное всегда начинается с префикса `Az`.</span><span class="sxs-lookup"><span data-stu-id="69fae-128">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="69fae-129">Полный список стандартных глаголов см. в разделе [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Утвержденные глаголы для команд PowerShell).</span><span class="sxs-lookup"><span data-stu-id="69fae-129">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="69fae-130">Если вы знаете существительные и глаголы, с помощью модулей Azure PowerShell можно найти команды, выполнив командлет [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="69fae-130">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="69fae-131">Например, чтобы найти все связанные с виртуальной машиной команды, в которых используется глагол `Get` выполните следующий код:</span><span class="sxs-lookup"><span data-stu-id="69fae-131">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="69fae-132">Чтобы облегчить поиск часто используемых команд, в таблице ниже приведены типы ресурсов, указан соответствующий модуль Azure PowerShell и префикс для использования с командой `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="69fae-132">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="69fae-133">Тип ресурса</span><span class="sxs-lookup"><span data-stu-id="69fae-133">Resource type</span></span> | <span data-ttu-id="69fae-134">модуль Azure PowerShell;</span><span class="sxs-lookup"><span data-stu-id="69fae-134">Azure PowerShell module</span></span> | <span data-ttu-id="69fae-135">Префикс в существительном</span><span class="sxs-lookup"><span data-stu-id="69fae-135">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="69fae-136">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="69fae-136">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="69fae-137">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="69fae-137">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="69fae-138">Виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="69fae-138">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="69fae-139">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="69fae-139">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="69fae-140">Учетные записи хранения</span><span class="sxs-lookup"><span data-stu-id="69fae-140">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="69fae-141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="69fae-141">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="69fae-142">хранилище ключей;</span><span class="sxs-lookup"><span data-stu-id="69fae-142">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="69fae-143">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="69fae-143">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="69fae-144">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="69fae-144">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="69fae-145">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="69fae-145">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="69fae-146">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="69fae-146">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="69fae-147">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="69fae-147">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="69fae-148">Полный список модулей для Azure PowerShell см. на [этой странице](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) сайта GitHub.</span><span class="sxs-lookup"><span data-stu-id="69fae-148">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="69fae-149">Дополнительные сведения об основах работы с Azure PowerShell приведены в кратких руководствах и других материалах</span><span class="sxs-lookup"><span data-stu-id="69fae-149">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="69fae-150">Чтобы начать работу с Azure PowerShell, ознакомьтесь с подробным руководством по настройке виртуальных машин и отправке запросов на получение данных.</span><span class="sxs-lookup"><span data-stu-id="69fae-150">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="69fae-151">Создание виртуальных машин с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="69fae-151">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="69fae-152">Кроме того, можно воспользоваться краткими руководствами по Azure PowerShell для других популярных служб Azure:</span><span class="sxs-lookup"><span data-stu-id="69fae-152">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="69fae-153">создать учетную запись хранения;</span><span class="sxs-lookup"><span data-stu-id="69fae-153">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="69fae-154">Передача объектов в хранилище BLOB-объектов Azure и из него</span><span class="sxs-lookup"><span data-stu-id="69fae-154">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="69fae-155">Создание и извлечение секретов из Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="69fae-155">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="69fae-156">Создание базы данных Azure SQL и брандмауэра</span><span class="sxs-lookup"><span data-stu-id="69fae-156">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="69fae-157">Запуск контейнеров в службе "Экземпляры контейнеров Azure"</span><span class="sxs-lookup"><span data-stu-id="69fae-157">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="69fae-158">Создание масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="69fae-158">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="69fae-159">Создание подсистемы балансировки нагрузки уровня "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="69fae-159">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="69fae-160">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="69fae-160">Next steps</span></span>

* [<span data-ttu-id="69fae-161">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="69fae-161">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="69fae-162">Управление подписками Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="69fae-162">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="69fae-163">Создание субъектов-служб Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="69fae-163">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="69fae-164">Помощь от сообщества:</span><span class="sxs-lookup"><span data-stu-id="69fae-164">Get help from the community:</span></span>
  * [<span data-ttu-id="69fae-165">Форум Azure на MSDN</span><span class="sxs-lookup"><span data-stu-id="69fae-165">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="69fae-166">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="69fae-166">Stack Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
