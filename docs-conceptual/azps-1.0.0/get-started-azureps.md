---
title: Начало работы с Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 10/30/2018
ms.openlocfilehash: 7367648a0a84cd5be5c7501ef4bf743a4290ce0f
ms.sourcegitcommit: 6685809f054203bd733c84f68acc69e53e5cca8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/02/2019
ms.locfileid: "53982915"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="176d5-102">Начало работы с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="176d5-102">Get started with Azure PowerShell</span></span>

<span data-ttu-id="176d5-103">Модуль Azure PowerShell предназначен для администрирования ресурсов Azure из командной строки, а также для создания скриптов автоматизации, которые работают с Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="176d5-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="176d5-104">Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="176d5-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="176d5-105">В этой статье содержатся инструкции по началу работы с Azure PowerShell и объясняются основные принципы работы этого модуля.</span><span class="sxs-lookup"><span data-stu-id="176d5-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="176d5-106">Установите Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="176d5-106">Install Azure PowerShell</span></span>

<span data-ttu-id="176d5-107">Сначала установите последнюю версию модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="176d5-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="176d5-108">Сведения о последнем выпуске см. в [заметках о выпуске](./release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="176d5-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="176d5-109">[Установите Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="176d5-109">[Install Azure PowerShell](install-az-ps.md).</span></span>

2. <span data-ttu-id="176d5-110">Чтобы проверить установку, выполните `Get-InstalledModule Az -AllVersions` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="176d5-110">To verify the installation was successful, run `Get-InstalledModule Az -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="176d5-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="176d5-111">Azure Cloud Shell</span></span>

<span data-ttu-id="176d5-112">Самый простой способ начать работу — [запустить службу Cloud Shell](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="176d5-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="176d5-113">Запустите Cloud Shell с верхней панели навигации портала Azure.</span><span class="sxs-lookup"><span data-stu-id="176d5-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Значок оболочки](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="176d5-115">Выберите нужную подписку и создайте учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="176d5-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Создание учетной записи хранения](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="176d5-117">Когда хранилище будет создано, Cloud Shell откроет сеанс PowerShell в браузере.</span><span class="sxs-lookup"><span data-stu-id="176d5-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![Использование Cloud Shell с PowerShell](~/media/get-started-azureps/cloud-powershell.png)

## <a name="sign-in-to-azure"></a><span data-ttu-id="176d5-119">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="176d5-119">Sign in to Azure</span></span>

<span data-ttu-id="176d5-120">Войдите в интерактивном режиме:</span><span class="sxs-lookup"><span data-stu-id="176d5-120">Sign on interactively:</span></span>

1. <span data-ttu-id="176d5-121">Введите `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="176d5-121">Type `Connect-AzAccount`.</span></span> <span data-ttu-id="176d5-122">Аргумент `-Environment` позволяет выполнять аутентификацию для другого региона или облака.</span><span class="sxs-lookup"><span data-stu-id="176d5-122">The `-Environment` argument lets you authenticate for a different region or cloud.</span></span> <span data-ttu-id="176d5-123">Например, чтобы подключиться к Azure для Китая:</span><span class="sxs-lookup"><span data-stu-id="176d5-123">For example, to connect to Azure China:</span></span>

    ```powershell-interactive
    Connect-AzAccount -Environment AzureChinaCloud
    ```

2. <span data-ttu-id="176d5-124">Вы получите токен, используемый на https://microsoft.com/devicelogin.</span><span class="sxs-lookup"><span data-stu-id="176d5-124">You'll get a token to use on https://microsoft.com/devicelogin.</span></span> <span data-ttu-id="176d5-125">Откройте эту страницу в браузере и введите токен, чтобы войти с учетными данными Azure и авторизовать Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="176d5-125">Open this page in your browser and enter the token to sign in with your Azure credentials, and authorize Azure PowerShell.</span></span> 

<span data-ttu-id="176d5-126">После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для работы с ресурсами в подписке и управления ими.</span><span class="sxs-lookup"><span data-stu-id="176d5-126">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span> <span data-ttu-id="176d5-127">Дополнительные сведения о процессе входа и доступных методах проверки подлинности см. в статье [Sign in with Azure PowerShell](authenticate-azureps.md) (Вход с помощью Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="176d5-127">To learn more about the sign in process and available authentication methods, see [Sign in with Azure PowerShell](authenticate-azureps.md).</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="176d5-128">Создание виртуальной машины Windows с помощью простых значений по умолчанию</span><span class="sxs-lookup"><span data-stu-id="176d5-128">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="176d5-129">У командлета `New-AzVM` упрощенный синтаксис, что облегчает создание виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="176d5-129">The `New-AzVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="176d5-130">Вам нужно указать только два значения параметров: имя виртуальной машины и учетные данные локального администратора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="176d5-130">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="176d5-131">Сначала мы создадим объект учетных данных.</span><span class="sxs-lookup"><span data-stu-id="176d5-131">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="176d5-132">Затем — виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="176d5-132">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="176d5-133">Может возникнуть вопрос, что при этом еще создается, а также как настроена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="176d5-133">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="176d5-134">Сначала посмотрим на наши группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176d5-134">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="176d5-135">Группа ресурсов **cloud-shell-storage-westus** создается при первом использовании Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="176d5-135">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="176d5-136">Группа ресурсов **SampleVM** создается командлетом `New-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="176d5-136">The **SampleVM** resource group was created by the `New-AzVM` cmdlet.</span></span>

<span data-ttu-id="176d5-137">Но какие же ресурсы созданы в этой новой группе ресурсов?</span><span class="sxs-lookup"><span data-stu-id="176d5-137">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="176d5-138">Давайте получим дополнительные сведения о виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="176d5-138">Let's get some more details about the VM.</span></span> <span data-ttu-id="176d5-139">В этом примере показано, как получить сведения об образе операционной системы, который используется для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="176d5-139">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="176d5-140">Создание полностью настроенной виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="176d5-140">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="176d5-141">В предыдущем примере для создания виртуальной машины Windows используется упрощенный синтаксис и значения параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="176d5-141">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="176d5-142">В этом примере мы предоставляем значения для всех параметров виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="176d5-142">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="176d5-143">Создание группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="176d5-143">Create a resource group</span></span>

<span data-ttu-id="176d5-144">В этом примере показано, как создать группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176d5-144">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="176d5-145">Группы ресурсов в Azure позволяют управлять разными ресурсами, которые вы хотите логически сгруппировать.</span><span class="sxs-lookup"><span data-stu-id="176d5-145">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="176d5-146">Например, вы можете создать группу ресурсов для приложения или проекта, а затем добавить в эту группу виртуальную машину, базу данных и службу CDN.</span><span class="sxs-lookup"><span data-stu-id="176d5-146">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="176d5-147">Создайте группу ресурсов с именем MyResourceGroup в регионе Azure uswest2.</span><span class="sxs-lookup"><span data-stu-id="176d5-147">Let's create a resource group named "MyResourceGroup" in the uswest2 region of Azure.</span></span> <span data-ttu-id="176d5-148">Используйте для этого следующую команду:</span><span class="sxs-lookup"><span data-stu-id="176d5-148">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzResourceGroup -Name 'myResourceGroup' -Location 'westus2'
```

```output
ResourceGroupName : myResourceGroup
Location          : westus2
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="176d5-149">Эта новая группа ресурсов будет использоваться для размещения всех ресурсов, необходимых для создаваемой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="176d5-149">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="176d5-150">Чтобы создать виртуальную машину Linux, сначала нужно создать необходимые ресурсы и включить их в конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="176d5-150">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="176d5-151">Затем эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="176d5-151">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="176d5-152">Кроме того, вам потребуется открытый ключ SSH `id_rsa.pub` в каталоге `.ssh` вашего профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="176d5-152">Also, you will need to have an SSH public key named `id_rsa.pub` in the `.ssh` directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="176d5-153">Создание необходимых сетевых ресурсов</span><span class="sxs-lookup"><span data-stu-id="176d5-153">Create the required network resources</span></span>

<span data-ttu-id="176d5-154">Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="176d5-154">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="176d5-155">Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="176d5-155">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="176d5-156">Создайте группу безопасности сети для защиты доступа к общедоступному адресу.</span><span class="sxs-lookup"><span data-stu-id="176d5-156">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="176d5-157">Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="176d5-157">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westus2"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="176d5-158">Создание конфигурации виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="176d5-158">Create the VM configuration</span></span>

<span data-ttu-id="176d5-159">Теперь, когда у вас есть необходимые ресурсы, можно создать объект конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="176d5-159">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzVMConfig -VMName $vmName -VMSize Standard_B1s |
  Set-AzVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="176d5-160">Создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="176d5-160">Create the virtual machine</span></span>

<span data-ttu-id="176d5-161">Теперь мы можем создать виртуальную машину, используя объект конфигурации.</span><span class="sxs-lookup"><span data-stu-id="176d5-161">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="176d5-162">Вы можете войти в созданную виртуальную машину Linux, используя SSH и общедоступный IP-адрес этой виртуальной машины:</span><span class="sxs-lookup"><span data-stu-id="176d5-162">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```powershell-interactive
ssh azureuser@$($publicIp.IpAddress)
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="176d5-163">Создание других ресурсов в Azure</span><span class="sxs-lookup"><span data-stu-id="176d5-163">Creating other resources in Azure</span></span>

<span data-ttu-id="176d5-164">Вы узнали, как создавать группы ресурсов, а также виртуальные машины Linux и Windows Server.</span><span class="sxs-lookup"><span data-stu-id="176d5-164">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="176d5-165">Но вы также можете создать в Azure много других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176d5-165">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="176d5-166">Например, чтобы создать подсистему балансировки нагрузки Azure, которую можно затем связать с новой виртуальной машиной, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="176d5-166">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westus2
```

<span data-ttu-id="176d5-167">Также для своей инфраструктуры вы можете создать новую частную виртуальную сеть, используя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="176d5-167">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzVirtualNetwork -ResourceGroupName myResourceGroup -Location westus2 `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="176d5-168">Преимущество Azure и Azure PowerShell заключается в том, что их можно использовать для создания как облачной инфраструктуры, так и управляемых служб платформы.</span><span class="sxs-lookup"><span data-stu-id="176d5-168">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="176d5-169">Управляемые службы платформы также можно объединять с инфраструктурой, создавая еще более мощные решения.</span><span class="sxs-lookup"><span data-stu-id="176d5-169">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="176d5-170">Например, используя Azure PowerShell, вы можете создать службу приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="176d5-170">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="176d5-171">Служба приложений Azure — это управляемая служба платформы, на которой можно размещать веб-приложения, не беспокоясь об инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="176d5-171">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="176d5-172">Создав службу приложений Azure, вы можете создать два новых веб-приложения Azure с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="176d5-172">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Get a UUID for creating the apps to avoid name conflicts
$guid = [System.Guid]::NewGuid().ToString()

# Create an Azure AppService that we can host any number of web apps within
New-AzAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westus2

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzWebApp -Name MyWebApp-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
New-AzWebApp -Name MyWebApp2-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="176d5-173">Отображение списка развернутых ресурсов</span><span class="sxs-lookup"><span data-stu-id="176d5-173">Listing deployed resources</span></span>

<span data-ttu-id="176d5-174">Чтобы вывести список ресурсов, работающих в Azure, используйте командлет `Get-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="176d5-174">You can use the `Get-AzResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="176d5-175">В следующем примере показаны созданные ресурсы в новой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176d5-175">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westus2 Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westus2 Microsoft.Compute/disks
myLinuxVM                                             westus2 Microsoft.Compute/virtualMachines
myWindowsVM                                           westus2 Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westus2 Microsoft.Compute/virtualMachines/extensions
myNic1                                                westus2 Microsoft.Network/networkInterfaces
myNic2                                                westus2 Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westus2 Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westus2 Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westus2 Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westus2 Microsoft.Network/publicIPAddresses
MYvNET1                                               westus2 Microsoft.Network/virtualNetworks
MYvNET2                                               westus2 Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westus2 Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="176d5-176">Удаление ресурсов</span><span class="sxs-lookup"><span data-stu-id="176d5-176">Deleting resources</span></span>

<span data-ttu-id="176d5-177">Чтобы очистить учетную запись Azure, необходимо удалить ресурсы, созданные в этом примере.</span><span class="sxs-lookup"><span data-stu-id="176d5-177">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="176d5-178">Используйте командлеты `Remove-Az*` для удаления ресурсов, которые больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="176d5-178">You can use the `Remove-Az*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="176d5-179">Чтобы удалить виртуальную машину Windows, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="176d5-179">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="176d5-180">Вам будет предложено подтвердить удаление указанного ресурса.</span><span class="sxs-lookup"><span data-stu-id="176d5-180">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="176d5-181">Также за один раз можно удалить несколько ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176d5-181">You can also delete many resources at once.</span></span> <span data-ttu-id="176d5-182">Например, следующая команда удаляет группу ресурсов MyResourceGroup, которую мы использовали во всех предыдущих примерах.</span><span class="sxs-lookup"><span data-stu-id="176d5-182">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="176d5-183">Все ресурсы в группе также будут удалены.</span><span class="sxs-lookup"><span data-stu-id="176d5-183">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="176d5-184">Задача может занять несколько минут, в зависимости от количества и типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="176d5-184">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="176d5-185">Получение примеров</span><span class="sxs-lookup"><span data-stu-id="176d5-185">Get samples</span></span>

<span data-ttu-id="176d5-186">Дополнительные сведения о способах использования Azure PowerShell см. в примерах популярных сценариев для [виртуальных машин Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [виртуальных машин Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [веб-приложений](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) и [баз данных SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="176d5-186">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="176d5-187">Дополнительная информация</span><span class="sxs-lookup"><span data-stu-id="176d5-187">Next steps</span></span>

* [<span data-ttu-id="176d5-188">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="176d5-188">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="176d5-189">Управление подписками Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="176d5-189">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="176d5-190">Создание субъектов-служб в Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="176d5-190">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="176d5-191">Помощь от сообщества:</span><span class="sxs-lookup"><span data-stu-id="176d5-191">Get help from the community:</span></span>
  * [<span data-ttu-id="176d5-192">Форум Azure на MSDN</span><span class="sxs-lookup"><span data-stu-id="176d5-192">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="176d5-193">Stackoverflow</span><span class="sxs-lookup"><span data-stu-id="176d5-193">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
