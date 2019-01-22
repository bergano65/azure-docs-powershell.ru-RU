---
title: Начало работы с Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 483e74d7d047562b1c170c3767495161b9c5eb2f
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342136"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="ab551-102">Начало работы с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab551-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="ab551-103">Среда Azure PowerShell оптимизирована для администрирования ресурсов Azure и управления ими из командной строки.</span><span class="sxs-lookup"><span data-stu-id="ab551-103">Azure PowerShell is designed for managing and administering Azure resources from the command line.</span></span> <span data-ttu-id="ab551-104">С помощью Azure PowerShell можно создавать автоматизированные средства на основе модели Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ab551-104">Use Azure PowerShell when you want to build automated tools that use the Azure Resource Manager model.</span></span>
<span data-ttu-id="ab551-105">Попробуйте использовать его в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ab551-105">Try it out in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or install on your local machine.</span></span>

<span data-ttu-id="ab551-106">В этой статье содержатся инструкции по началу работы с Azure PowerShell и объясняются основные принципы работы этой среды.</span><span class="sxs-lookup"><span data-stu-id="ab551-106">This article helps you get started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-or-run-in-azure-cloud-shell"></a><span data-ttu-id="ab551-107">Установка или запуск в Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="ab551-107">Install or run in Azure Cloud Shell</span></span>

<span data-ttu-id="ab551-108">Проще всего начать работу с Azure PowerShell в среде Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="ab551-108">The easiest way to get started with Azure PowerShell is by trying it out in an Azure Cloud Shell environment.</span></span>
<span data-ttu-id="ab551-109">Чтобы скачать PowerShell и начать работу с Cloud Shell, см. [краткое руководство по использованию PowerShell в Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="ab551-109">To get up and running with Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
<span data-ttu-id="ab551-110">Cloud Shell запускает PowerShell 6 в контейнере Linux, поэтому специальные функции Windows будут недоступны.</span><span class="sxs-lookup"><span data-stu-id="ab551-110">Cloud Shell runs PowerShell 6 on a Linux container, so Windows-specific functionality isn't available.</span></span>

<span data-ttu-id="ab551-111">Когда все будет готово к установке Azure PowerShell на локальный компьютер, следуйте инструкциям, приведенным в статье [Install the Azure PowerShell module](install-az-ps.md) (Установка модуля Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="ab551-111">When you're ready to install Azure PowerShell on your local machine, follow the instructions in [Install the Azure PowerShell module](install-az-ps.md).</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="ab551-112">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="ab551-112">Sign in to Azure</span></span>

<span data-ttu-id="ab551-113">Войдите в учетную запись в интерактивном режиме с помощью командлета `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="ab551-113">Sign in interactively with the `Connect-AzAccount` cmdlet.</span></span> <span data-ttu-id="ab551-114">При использовании Cloud Shell этот шаг можно пропустить: Для сеанса Auzre Cloud Shell уже выполнена проверка подлинности для среды, подписки и клиента, который запустил сеанс Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="ab551-114">Skip this step if you use Cloud Shell: Your Auzre Cloud Shell session is already authenticated for the environment, subscription, and tenant that launched the Cloud Shell session.</span></span>

```azurepowershell-interactive
Connect-AzAccount
```

<span data-ttu-id="ab551-115">Если вы находитесь за пределами США, используйте для входа параметр `-Environment`.</span><span class="sxs-lookup"><span data-stu-id="ab551-115">If you're in a non-US region, use the `-Environment` parameter to sign in.</span></span> <span data-ttu-id="ab551-116">Имя среды для вашего региона можно получить с помощью командлета [Get AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).</span><span class="sxs-lookup"><span data-stu-id="ab551-116">Get the name of the environment for your region by using the [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment) cmdlet.</span></span> <span data-ttu-id="ab551-117">Например, для входа в учетную запись Azure China 21Vianet выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="ab551-117">For example, to sign in to Azure China 21Vianet:</span></span>

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

<span data-ttu-id="ab551-118">Вы получите токен, используемый на https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="ab551-118">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="ab551-119">Откройте эту страницу в браузере и введите токен, чтобы войти с данными учетной записи Azure и авторизовать Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ab551-119">Open this page in your browser and enter the token, then sign in with your Azure account credentials and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="ab551-120">После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для доступа и управления ресурсами в подписке.</span><span class="sxs-lookup"><span data-stu-id="ab551-120">Once signed in, use the Azure PowerShell cmdlets to access and manage resources in your subscription.</span></span> <span data-ttu-id="ab551-121">Дополнительные сведения о процессе входа и методах проверки подлинности см. в статье [Вход с помощью Azure PowerShell](authenticate-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ab551-121">To learn more about the sign-in process and authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="find-commands"></a><span data-ttu-id="ab551-122">Поиск команд</span><span class="sxs-lookup"><span data-stu-id="ab551-122">Find commands</span></span>

<span data-ttu-id="ab551-123">В Azure PowerShell названия командлетов выбираются в соответствии со стандартным соглашением об именовании для PowerShell — `VERB-NOUN`.</span><span class="sxs-lookup"><span data-stu-id="ab551-123">Azure PowerShell cmdlets follow a standard naming convention for PowerShell, `VERB-NOUN`.</span></span> <span data-ttu-id="ab551-124">Глагол (часть verb) отвечает за действие (к ним относятся `Create`, `Get`, `Set`, `Delete`), а существительное (часть noun) — за тип ресурса (к ним относятся `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span><span class="sxs-lookup"><span data-stu-id="ab551-124">The verb describes the action (examples include `Create`, `Get`, `Set`, `Delete`) and the noun describes the resource type (examples include `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`).</span></span> <span data-ttu-id="ab551-125">В Azure PowerShell существительное всегда начинается с префикса `Az`.</span><span class="sxs-lookup"><span data-stu-id="ab551-125">Nouns in Azure PowerShell always start with the prefix `Az`.</span></span> <span data-ttu-id="ab551-126">Полный список стандартных глаголов см. в разделе [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands) (Утвержденные глаголы для команд PowerShell).</span><span class="sxs-lookup"><span data-stu-id="ab551-126">For the full list of standard verbs, see [Approved verbs for PowerShell Commands](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).</span></span>

<span data-ttu-id="ab551-127">Если вы знаете существительные и глаголы, с помощью модулей Azure PowerShell можно найти команды, выполнив командлет [Get-Command](/powershell/module/microsoft.powershell.core/get-command).</span><span class="sxs-lookup"><span data-stu-id="ab551-127">Knowing the nouns, verbs, and the Azure PowerShell modules available help you find commands with the [Get-Command](/powershell/module/microsoft.powershell.core/get-command) cmdlet.</span></span> <span data-ttu-id="ab551-128">Например, чтобы найти все связанные с виртуальной машиной команды, в которых используется глагол `Get` выполните следующий код:</span><span class="sxs-lookup"><span data-stu-id="ab551-128">For example, to find all VM-related commands that use the `Get` verb:</span></span>

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

<span data-ttu-id="ab551-129">Чтобы облегчить поиск часто используемых команд, в таблице ниже приведены типы ресурсов, указан соответствующий модуль Azure PowerShell и префикс для использования с командой `Get-Command`:</span><span class="sxs-lookup"><span data-stu-id="ab551-129">To help you find common commands, this table lists the resource type, corresponding Azure PowerShell module, and noun prefix to use with `Get-Command`:</span></span>

| <span data-ttu-id="ab551-130">Тип ресурса</span><span class="sxs-lookup"><span data-stu-id="ab551-130">Resource type</span></span> | <span data-ttu-id="ab551-131">модуль Azure PowerShell;</span><span class="sxs-lookup"><span data-stu-id="ab551-131">Azure PowerShell module</span></span> | <span data-ttu-id="ab551-132">Префикс в существительном</span><span class="sxs-lookup"><span data-stu-id="ab551-132">Noun prefix</span></span> |
|---------------|-------------------------|----------------|
| [<span data-ttu-id="ab551-133">Группа ресурсов</span><span class="sxs-lookup"><span data-stu-id="ab551-133">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="ab551-134">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab551-134">Az.Resources</span></span>](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [<span data-ttu-id="ab551-135">Виртуальные машины</span><span class="sxs-lookup"><span data-stu-id="ab551-135">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="ab551-136">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab551-136">Az.Compute</span></span>](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [<span data-ttu-id="ab551-137">Учетные записи хранения</span><span class="sxs-lookup"><span data-stu-id="ab551-137">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="ab551-138">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab551-138">Az.Storage</span></span>](/powershell/module/az.storage/) | `AzStorageAccount` |
| [<span data-ttu-id="ab551-139">хранилище ключей;</span><span class="sxs-lookup"><span data-stu-id="ab551-139">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="ab551-140">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab551-140">Az.KeyVault</span></span>](/powershell/module/az.keyvault) | `AzKeyVault` |
| [<span data-ttu-id="ab551-141">Веб-приложения</span><span class="sxs-lookup"><span data-stu-id="ab551-141">Web applications</span></span>](/azure/app-service) | [<span data-ttu-id="ab551-142">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab551-142">Az.Websites</span></span>](/powershell/module/az.websites) | `AzWebApp` |
| [<span data-ttu-id="ab551-143">Базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="ab551-143">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="ab551-144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab551-144">Az.Sql</span></span>](/powershell/module/az.sql) | `AzSqlDatabase` |

<span data-ttu-id="ab551-145">Полный список модулей для Azure PowerShell см. на [этой странице](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) сайта GitHub.</span><span class="sxs-lookup"><span data-stu-id="ab551-145">For a full list of the modules in Azure PowerShell, see the [Azure PowerShell modules list](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) hosted on GitHub.</span></span>

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="ab551-146">Дополнительные сведения об основах работы с Azure PowerShell приведены в кратких руководствах и других материалах</span><span class="sxs-lookup"><span data-stu-id="ab551-146">Learn Azure PowerShell basics with quickstarts and tutorials</span></span>

<span data-ttu-id="ab551-147">Чтобы начать работу с Azure PowerShell, ознакомьтесь с подробным руководством по настройке виртуальных машин и отправке запросов на получение данных.</span><span class="sxs-lookup"><span data-stu-id="ab551-147">To get started with Azure PowerShell, try an in-depth tutorial for setting up virtual machines and learning how to query them.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ab551-148">Создание виртуальных машин с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab551-148">Create virtual machines with Azure PowerShell</span></span>](azureps-vm-tutorial.yml)

<span data-ttu-id="ab551-149">Кроме того, можно воспользоваться краткими руководствами по Azure PowerShell для других популярных служб Azure:</span><span class="sxs-lookup"><span data-stu-id="ab551-149">There are also Azure PowerShell quickstarts for other popular Azure services:</span></span>

* [<span data-ttu-id="ab551-150">создать учетную запись хранения;</span><span class="sxs-lookup"><span data-stu-id="ab551-150">Create a storage account</span></span>](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [<span data-ttu-id="ab551-151">Передача объектов в хранилище BLOB-объектов Azure и из него</span><span class="sxs-lookup"><span data-stu-id="ab551-151">Transfer objects to/from Azure Blob storage</span></span>](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [<span data-ttu-id="ab551-152">Создание и извлечение секретов из Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="ab551-152">Create and retrieve secrets from Azure Key Vault</span></span>](/azure/key-vault/quick-create-powershell)
* [<span data-ttu-id="ab551-153">Создание базы данных Azure SQL и брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ab551-153">Create an Azure SQL database and firewall</span></span>](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [<span data-ttu-id="ab551-154">Запуск контейнеров в службе "Экземпляры контейнеров Azure"</span><span class="sxs-lookup"><span data-stu-id="ab551-154">Run a container in Azure Container Instances</span></span>](/azure/container-instances/container-instances-quickstart-powershell)
* [<span data-ttu-id="ab551-155">Создание масштабируемого набора виртуальных машин (VMSS)</span><span class="sxs-lookup"><span data-stu-id="ab551-155">Create a Virtual Machine Scale Set (VMSS)</span></span>](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [<span data-ttu-id="ab551-156">Создание подсистемы балансировки нагрузки уровня "Стандартный"</span><span class="sxs-lookup"><span data-stu-id="ab551-156">Create a standard load balancer</span></span>](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a><span data-ttu-id="ab551-157">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="ab551-157">Next steps</span></span>

* [<span data-ttu-id="ab551-158">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab551-158">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="ab551-159">Управление подписками Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab551-159">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="ab551-160">Создание субъектов-служб Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab551-160">Create service principals with Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="ab551-161">Помощь от сообщества:</span><span class="sxs-lookup"><span data-stu-id="ab551-161">Get help from the community:</span></span>
  * [<span data-ttu-id="ab551-162">Форум Azure на MSDN</span><span class="sxs-lookup"><span data-stu-id="ab551-162">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="ab551-163">Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="ab551-163">Stacki Overflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
