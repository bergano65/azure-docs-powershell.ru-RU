---
title: "<span data-ttu-id=\"29cec-101\">Начало работы с модулем Azure PowerShell | Документация Майкрософт</span><span class=\"sxs-lookup\"><span data-stu-id=\"29cec-101\">Get started with Azure PowerShell | Microsoft Docs</span></span>"
description: 
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 03/30/2017
ms.openlocfilehash: 4bfa14f4f139fa8c35d4bb51ae81baea819188ce
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2017
---
# <span data-ttu-id="29cec-102">Начало работы с Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="29cec-102">Getting started with Azure PowerShell</span></span>
<a id="getting-started-with-azure-powershell" class="xliff"></a>

<span data-ttu-id="29cec-103">Модуль Azure PowerShell предназначен для администрирования ресурсов Azure из командной строки, а также для создания скриптов автоматизации, которые работают с Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="29cec-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="29cec-104">Эта статья поможет приступить к работе с модулем и объяснит основные принципы его работы.</span><span class="sxs-lookup"><span data-stu-id="29cec-104">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>


## <span data-ttu-id="29cec-105">Установка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="29cec-105">Install Azure PowerShell</span></span>
<a id="install-azure-powershell" class="xliff"></a>
<span data-ttu-id="29cec-106">Сначала установите последнюю версию модуля Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="29cec-106">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span>  <span data-ttu-id="29cec-107">Это — версия 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="29cec-107">The latest version is 4.1.0.</span></span>

1. <span data-ttu-id="29cec-108">[Установите Azure PowerShell](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="29cec-108">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="29cec-109">Чтобы проверить установку, выполните `Get-Module AzureRM` в командной строке.</span><span class="sxs-lookup"><span data-stu-id="29cec-109">To verify the installation was successful, run `Get-Module AzureRM` from your command line.</span></span>


## <span data-ttu-id="29cec-110">Вход в Azure</span><span class="sxs-lookup"><span data-stu-id="29cec-110">Log in to Azure</span></span>
<a id="log-in-to-azure" class="xliff"></a>

<span data-ttu-id="29cec-111">Войдите в интерактивном режиме:</span><span class="sxs-lookup"><span data-stu-id="29cec-111">Sign on interactively:</span></span>

1. <span data-ttu-id="29cec-112">Введите `Login-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="29cec-112">Type `Login-AzureRmAccount`.</span></span>  <span data-ttu-id="29cec-113">Появится диалоговое окно с запросом на ввод учетных данных Azure.</span><span class="sxs-lookup"><span data-stu-id="29cec-113">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="29cec-114">С помощью параметра -EnvironmentName можно войти в Azure для Китая или Azure для Германии.</span><span class="sxs-lookup"><span data-stu-id="29cec-114">Option '-EnvironmentName' can let you login in Azure China or Azure Germany.</span></span>
   <span data-ttu-id="29cec-115">Пример: Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="29cec-115">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="29cec-116">Введите электронный адрес и пароль, связанные с вашей учетной записью.</span><span class="sxs-lookup"><span data-stu-id="29cec-116">Type the email address and password associated with your account.</span></span> <span data-ttu-id="29cec-117">Azure выполняет проверку подлинности и сохраняет учетные данные, а затем закрывает окно.</span><span class="sxs-lookup"><span data-stu-id="29cec-117">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="29cec-118">После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для доступа к ресурсам в подписке и управления ими.</span><span class="sxs-lookup"><span data-stu-id="29cec-118">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <span data-ttu-id="29cec-119">Создание группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="29cec-119">Create a resource group</span></span>
<a id="create-a-resource-group" class="xliff"></a>

<span data-ttu-id="29cec-120">Теперь, когда все настроено, вы можете создавать ресурсы в Azure с помощью Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="29cec-120">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="29cec-121">Сначала создайте группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29cec-121">First, create a Resource Group.</span></span> <span data-ttu-id="29cec-122">Группы ресурсов в Azure позволяют управлять разными ресурсами, которые вы хотите логически сгруппировать.</span><span class="sxs-lookup"><span data-stu-id="29cec-122">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="29cec-123">Например, вы можете создать группу ресурсов для приложения или проекта, а затем добавить в эту группу виртуальную машину, базу данных и службу CDN.</span><span class="sxs-lookup"><span data-stu-id="29cec-123">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="29cec-124">Создайте группу ресурсов с именем MyResourceGroup в регионе Azure "Западная Европа".</span><span class="sxs-lookup"><span data-stu-id="29cec-124">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="29cec-125">Используйте для этого следующую команду:</span><span class="sxs-lookup"><span data-stu-id="29cec-125">To do so type the following command:</span></span>

```powershell
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <span data-ttu-id="29cec-126">Создание виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="29cec-126">Create a Windows Virtual Machine</span></span>
<a id="create-a-windows-virtual-machine" class="xliff"></a>

<span data-ttu-id="29cec-127">Теперь, когда у вас есть группа ресурсов, создайте в ней виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="29cec-127">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="29cec-128">Чтобы создать виртуальную машину, сначала нужно создать необходимые ресурсы и назначить их в качестве конфигурации.</span><span class="sxs-lookup"><span data-stu-id="29cec-128">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="29cec-129">Затем эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="29cec-129">Then we can use that configuration to create the VM.</span></span>

### <span data-ttu-id="29cec-130">Создание необходимых сетевых ресурсов</span><span class="sxs-lookup"><span data-stu-id="29cec-130">Create the required network resources</span></span>
<a id="create-the-required-network-resources" class="xliff"></a>

<span data-ttu-id="29cec-131">Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="29cec-131">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="29cec-132">Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="29cec-132">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="29cec-133">Создайте группу безопасности сети для защиты доступа к общедоступному адресу.</span><span class="sxs-lookup"><span data-stu-id="29cec-133">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="29cec-134">Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="29cec-134">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <span data-ttu-id="29cec-135">Создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="29cec-135">Create the virtual machine</span></span>
<a id="create-the-virtual-machine" class="xliff"></a>

<span data-ttu-id="29cec-136">Сначала укажите учетные данные для операционной системы.</span><span class="sxs-lookup"><span data-stu-id="29cec-136">First we need a set of credentials for the OS.</span></span>

```powershell
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="29cec-137">Теперь, когда у вас есть необходимые ресурсы, можно создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="29cec-137">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="29cec-138">На этом шаге создайте объект конфигурации виртуальной машины. Потом эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="29cec-138">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="29cec-139">Команда `New-AzureRmVM` выводит результаты, когда виртуальная машина создана и готова к использованию.</span><span class="sxs-lookup"><span data-stu-id="29cec-139">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="29cec-140">Теперь войдите на созданную виртуальную машину Windows Server, используя протокол RDP и общедоступный IP-адрес этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="29cec-140">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="29cec-141">Следующая команда отображает общедоступный IP-адрес, созданный в предыдущем скрипте.</span><span class="sxs-lookup"><span data-stu-id="29cec-141">The following command displays the public IP address created in the previous script.</span></span>

```powershell
$publicIp | Select-Object Name,IpAddress
```

```
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="29cec-142">Если вы работаете на компьютере Windows, вы можете отобразить IP-адрес, выполнив команду mstsc в командной строке:</span><span class="sxs-lookup"><span data-stu-id="29cec-142">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="29cec-143">Для входа укажите те же учетные данные (имя пользователя и пароль), которые вы использовали при создании виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="29cec-143">Supply the same username/password combination you used when creating the VM to log in.</span></span>


## <span data-ttu-id="29cec-144">Создание виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="29cec-144">Create a Linux Virtual Machine</span></span>
<a id="create-a-linux-virtual-machine" class="xliff"></a>

<span data-ttu-id="29cec-145">Чтобы создать виртуальную машину Linux, сначала нужно создать необходимые ресурсы и назначить их в качестве конфигурации.</span><span class="sxs-lookup"><span data-stu-id="29cec-145">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="29cec-146">Затем эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="29cec-146">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="29cec-147">Предполагается, что вы уже создали группу ресурсов, как описано в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="29cec-147">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="29cec-148">Кроме того, вам потребуется открытый ключ SSH `id_rsa.pub` в каталоге формата SSH вашего профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="29cec-148">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <span data-ttu-id="29cec-149">Создание необходимых сетевых ресурсов</span><span class="sxs-lookup"><span data-stu-id="29cec-149">Create the required network resources</span></span>
<a id="create-the-required-network-resources" class="xliff"></a>

<span data-ttu-id="29cec-150">Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="29cec-150">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="29cec-151">Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="29cec-151">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="29cec-152">Создайте группу безопасности сети для защиты доступа к общедоступному адресу.</span><span class="sxs-lookup"><span data-stu-id="29cec-152">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="29cec-153">Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="29cec-153">Finally we create the virtual NIC using all of the previous resources.</span></span>

```powershell
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <span data-ttu-id="29cec-154">Создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="29cec-154">Create the virtual machine</span></span>
<a id="create-the-virtual-machine" class="xliff"></a>

<span data-ttu-id="29cec-155">Теперь, когда у вас есть необходимые ресурсы, можно создать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="29cec-155">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="29cec-156">На этом шаге создайте объект конфигурации виртуальной машины. Потом эту конфигурацию можно использовать для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="29cec-156">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="29cec-157">Вы можете войти на созданную виртуальную машину Linux, используя SSH и общедоступный IP-адрес этой виртуальной машины:</span><span class="sxs-lookup"><span data-stu-id="29cec-157">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```
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

my-login@MyLinuxVM:~$
```

## <span data-ttu-id="29cec-158">Создание других ресурсов в Azure</span><span class="sxs-lookup"><span data-stu-id="29cec-158">Creating other resources in Azure</span></span>
<a id="creating-other-resources-in-azure" class="xliff"></a>

<span data-ttu-id="29cec-159">Вы узнали, как создавать группы ресурсов, а также виртуальные машины Linux и Windows Server.</span><span class="sxs-lookup"><span data-stu-id="29cec-159">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="29cec-160">Но вы также можете создать в Azure много других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29cec-160">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="29cec-161">Например, чтобы создать подсистему балансировки нагрузки Azure, которую можно затем связать с новой виртуальной машиной, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="29cec-161">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="29cec-162">Также для своей инфраструктуры вы можете создать новую частную виртуальную сеть, используя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="29cec-162">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="29cec-163">Преимущество Azure и Azure PowerShell заключается в том, что их можно использовать для создания как облачной инфраструктуры, так и управляемых служб платформы.</span><span class="sxs-lookup"><span data-stu-id="29cec-163">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="29cec-164">Управляемые службы платформы также можно объединять с инфраструктурой, создавая еще более мощные решения.</span><span class="sxs-lookup"><span data-stu-id="29cec-164">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="29cec-165">Например, используя Azure PowerShell, вы можете создать службу приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="29cec-165">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="29cec-166">Служба приложений Azure — это управляемая служба платформы, на которой можно размещать веб-приложения, не беспокоясь об инфраструктуре.</span><span class="sxs-lookup"><span data-stu-id="29cec-166">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="29cec-167">Создав службу приложений Azure, вы можете создать два новых веб-приложения Azure с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="29cec-167">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <span data-ttu-id="29cec-168">Отображение списка развернутых ресурсов</span><span class="sxs-lookup"><span data-stu-id="29cec-168">Listing deployed resources</span></span>
<a id="listing-deployed-resources" class="xliff"></a>

<span data-ttu-id="29cec-169">Чтобы вывести список ресурсов, работающих в Azure, используйте командлет `Get-AzureRmResource`.</span><span class="sxs-lookup"><span data-stu-id="29cec-169">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="29cec-170">В следующем примере показаны ресурсы, входящие в созданную группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29cec-170">The following example shows the resources we just created in the new resource group.</span></span>

```powershell
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <span data-ttu-id="29cec-171">Удаление ресурсов</span><span class="sxs-lookup"><span data-stu-id="29cec-171">Deleting resources</span></span>
<a id="deleting-resources" class="xliff"></a>

<span data-ttu-id="29cec-172">Чтобы очистить учетную запись Azure, необходимо удалить ресурсы, созданные в этом примере.</span><span class="sxs-lookup"><span data-stu-id="29cec-172">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="29cec-173">Используйте командлеты `Remove-AzureRm*` для удаления ресурсов, которые больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="29cec-173">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="29cec-174">Чтобы удалить виртуальную машину Windows, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="29cec-174">To remove the Windows VM we created, using the following command:</span></span>

```powershell
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="29cec-175">Вам будет предложено подтвердить удаление указанных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29cec-175">You will be prompted to confirm that you want to remove the resource.</span></span>

```
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="29cec-176">Также можно удалить несколько ресурсов одновременно.</span><span class="sxs-lookup"><span data-stu-id="29cec-176">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="29cec-177">Например, следующая команда удаляет всю группу ресурсов MyResourceGroup, связанную со всеми примерами в этом руководстве по началу работы.</span><span class="sxs-lookup"><span data-stu-id="29cec-177">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="29cec-178">Эта команда удаляет группу ресурсов и все ресурсы, которые группа содержит.</span><span class="sxs-lookup"><span data-stu-id="29cec-178">This removes the resource group and all of the resources in it.</span></span>

```powershell
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="29cec-179">Это может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="29cec-179">This can take several minutes to complete.</span></span>

## <span data-ttu-id="29cec-180">Получение примеров</span><span class="sxs-lookup"><span data-stu-id="29cec-180">Get samples</span></span>
<a id="get-samples" class="xliff"></a>

<span data-ttu-id="29cec-181">Дополнительные сведения о способах использования Azure PowerShell см. в примерах популярных сценариев для [виртуальных машин Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [виртуальных машин Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [веб-приложений](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) и [баз данных SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="29cec-181">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <span data-ttu-id="29cec-182">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="29cec-182">Next steps</span></span>
<a id="next-steps" class="xliff"></a>

* [<span data-ttu-id="29cec-183">Вход с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="29cec-183">Login with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="29cec-184">Управление подписками Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="29cec-184">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="29cec-185">Создание субъектов-служб в Azure с помощью Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="29cec-185">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="29cec-186">См. заметки о выпуске, связанные с миграцией из старой версии: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="29cec-186">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="29cec-187">Помощь от сообщества:</span><span class="sxs-lookup"><span data-stu-id="29cec-187">Get help from the community:</span></span>
  + [<span data-ttu-id="29cec-188">Форум Azure на MSDN</span><span class="sxs-lookup"><span data-stu-id="29cec-188">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  + [<span data-ttu-id="29cec-189">Stackoverflow</span><span class="sxs-lookup"><span data-stu-id="29cec-189">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
