---
title: Начало работы с Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 5354a75e969e084d6457d0566a516705f365476f
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2018
ms.locfileid: "43018847"
---
# <a name="get-started-with-azure-powershell"></a>Начало работы с Azure PowerShell

Модуль Azure PowerShell предназначен для администрирования ресурсов Azure из командной строки, а также для создания скриптов автоматизации, которые работают с Azure Resource Manager. Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере. В этой статье содержатся инструкции по началу работы с Azure PowerShell и объясняются основные принципы работы этого модуля.

## <a name="install-azure-powershell"></a>Установите Azure PowerShell

Сначала установите последнюю версию модуля Azure PowerShell. Сведения о последнем выпуске см. в [заметках о выпуске](./release-notes-azureps.md).

1. [Установите Azure PowerShell](install-azurerm-ps.md).

2. Чтобы проверить установку, выполните `Get-Module AzureRM -ListAvailable` в командной строке.

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

Самый простой способ начать работу — [запустить службу Cloud Shell](/azure/cloud-shell/quickstart).

1. Запустите Cloud Shell с верхней панели навигации портала Azure.

   ![Значок оболочки](~/media/get-started-azureps/shell-icon.png)

2. Выберите нужную подписку и создайте учетную запись хранения.

   ![Создание учетной записи хранения](~/media/get-started-azureps/storage-prompt.png)

Когда хранилище будет создано, Cloud Shell откроет сеанс PowerShell в браузере.

![Использование Cloud Shell с PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Вы также можете установить Azure PowerShell для локального использования в сеансе PowerShell.

## <a name="sign-in-to-azure"></a>Вход в Azure

Войдите в интерактивном режиме:

1. Введите `Connect-AzureRmAccount`. Появится диалоговое окно с запросом на ввод учетных данных Azure. С помощью параметра -Environment можно пройти проверку подлинности в Azure для Китая или Azure для Германии.

   Пример: Connect-AzureRmAccount -Environment AzureChinaCloud

2. Введите электронный адрес и пароль, связанные с вашей учетной записью. Azure выполняет проверку подлинности и сохраняет учетные данные, а затем закрывает окно.

После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для работы с ресурсами в подписке и управления ими.

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>Создание виртуальной машины Windows с помощью простых значений по умолчанию

У командлета `New-AzureRmVM` упрощенный синтаксис, что облегчает создание виртуальной машины. Вам нужно указать только два значения параметров: имя виртуальной машины и учетные данные локального администратора виртуальной машины.

Сначала мы создадим объект учетных данных.

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

Затем — виртуальную машину.

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
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

Это достаточно просто. Но может возникнуть вопрос, что при этом еще создается, а также как настроена виртуальная машина. Сначала посмотрим на наши группы ресурсов.

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

Группа ресурсов **cloud-shell-storage-westus** создается при первом использовании Cloud Shell. Группа ресурсов **SampleVM** создается командлетом `New-AzureRmVM`.

Но какие же ресурсы созданы в этой новой группе ресурсов?

```azurepowershell-interactive
Get-AzureRmResource |
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

Давайте получим дополнительные сведения о виртуальной машине. В этих примерах показано, как получить сведения об образе операционной системы, используемом для создания виртуальной машины.

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
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

## <a name="create-a-fully-configured-linux-virtual-machine"></a>Создание полностью настроенной виртуальной машины Linux

В предыдущем примере для создания виртуальной машины Windows используется упрощенный синтаксис и значения параметров по умолчанию. В этом примере мы предоставляем значения для всех параметров виртуальной машины.

### <a name="create-a-resource-group"></a>Создание группы ресурсов

В этом примере мы создадим группу ресурсов. Группы ресурсов в Azure позволяют управлять разными ресурсами, которые вы хотите логически сгруппировать. Например, вы можете создать группу ресурсов для приложения или проекта, а затем добавить в эту группу виртуальную машину, базу данных и службу CDN.

Создайте группу ресурсов с именем MyResourceGroup в регионе Azure "Западная Европа". Используйте для этого следующую команду:

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

Эта новая группа ресурсов будет использоваться для размещения всех ресурсов, необходимых для создаваемой виртуальной машины. Чтобы создать виртуальную машину Linux, сначала нужно создать необходимые ресурсы и назначить их в качестве конфигурации. Затем эту конфигурацию можно использовать для создания виртуальной машины. Кроме того, вам потребуется открытый ключ SSH `id_rsa.pub` в каталоге формата SSH вашего профиля пользователя.

#### <a name="create-the-required-network-resources"></a>Создание необходимых сетевых ресурсов

Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети. Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине. Создайте группу безопасности сети для защиты доступа к общедоступному адресу. Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
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

### <a name="create-the-vm-configuration"></a>Создание конфигурации виртуальной машины

Теперь, когда у вас есть необходимые ресурсы, можно создать объект конфигурации виртуальной машины.

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a>Создание виртуальной машины

Теперь мы можем создать виртуальную машину, используя объект конфигурации.

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Вы можете войти на созданную виртуальную машину Linux, используя SSH и общедоступный IP-адрес этой виртуальной машины:

```bash
ssh xx.xxx.xxx.xxx
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

## <a name="creating-other-resources-in-azure"></a>Создание других ресурсов в Azure

Вы узнали, как создавать группы ресурсов, а также виртуальные машины Linux и Windows Server. Но вы также можете создать в Azure много других ресурсов.

Например, чтобы создать подсистему балансировки нагрузки Azure, которую можно затем связать с новой виртуальной машиной, выполните следующую команду:

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Также для своей инфраструктуры вы можете создать новую частную виртуальную сеть, используя следующую команду:

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Преимущество Azure и Azure PowerShell заключается в том, что их можно использовать для создания как облачной инфраструктуры, так и управляемых служб платформы. Управляемые службы платформы также можно объединять с инфраструктурой, создавая еще более мощные решения.

Например, используя Azure PowerShell, вы можете создать службу приложений Azure. Служба приложений Azure — это управляемая служба платформы, на которой можно размещать веб-приложения, не беспокоясь об инфраструктуре. Создав службу приложений Azure, вы можете создать два новых веб-приложения Azure с помощью следующих команд:

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Отображение списка развернутых ресурсов

Чтобы вывести список ресурсов, работающих в Azure, используйте командлет `Get-AzureRmResource`. В следующем примере показаны ресурсы, входящие в созданную группу ресурсов.

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
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

## <a name="deleting-resources"></a>Удаление ресурсов

Чтобы очистить учетную запись Azure, необходимо удалить ресурсы, созданные в этом примере. Используйте командлеты `Remove-AzureRm*` для удаления ресурсов, которые больше не нужны. Чтобы удалить виртуальную машину Windows, выполните следующую команду:

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Вам будет предложено подтвердить удаление указанных ресурсов.

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Также можно удалить несколько ресурсов одновременно. Например, следующая команда удаляет всю группу ресурсов MyResourceGroup, связанную со всеми примерами в этом руководстве по началу работы. Эта команда удаляет группу ресурсов и все ресурсы, которые группа содержит.

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Это может занять несколько минут.

## <a name="get-samples"></a>Получение примеров

Дополнительные сведения о способах использования Azure PowerShell см. в примерах популярных сценариев для [виртуальных машин Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [виртуальных машин Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [веб-приложений](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) и [баз данных SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Дополнительная информация

* [Вход с помощью Azure PowerShell](authenticate-azureps.md)
* [Управление подписками Azure с помощью Azure PowerShell](manage-subscriptions-azureps.md)
* [Создание субъектов-служб в Azure с помощью Azure PowerShell](create-azure-service-principal-azureps.md)
* Ознакомьтесь с заметками о выпуске, касающимися миграции с более ранней версии: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Помощь от сообщества:
  * [Форум Azure на MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
