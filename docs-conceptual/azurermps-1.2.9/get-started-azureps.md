---
title: Начало работы с модулем Azure PowerShell | Документация Майкрософт
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 3a0d3d1d970f4458e66167fb55c840598ce59e13
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854534"
---
# <a name="getting-started-with-azure-powershell"></a>Начало работы с Azure PowerShell

Модуль Azure PowerShell предназначен для администрирования ресурсов Azure из командной строки, а также для создания скриптов автоматизации, которые работают с Azure Resource Manager. Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере и использовать в любом сеансе PowerShell. Эта статья поможет приступить к работе с модулем и объяснит основные принципы его работы.

## <a name="connect"></a>Подключение

Самый простой способ начать работу — [запустить службу Cloud Shell](/azure/cloud-shell/quickstart).

1. Запустите Cloud Shell с верхней панели навигации портала Azure.

   ![Значок оболочки](~/media/get-started-azureps/shell-icon.png)

2. Выберите нужную подписку и создайте учетную запись хранения.

   ![Создание учетной записи хранения](~/media/get-started-azureps/storage-prompt.png)

Когда хранилище будет создано, Cloud Shell откроет сеанс PowerShell в браузере.

![Использование Cloud Shell с PowerShell](~/media/get-started-azureps/cloud-powershell.png)

Вы также можете установить Azure PowerShell для локального использования в сеансе PowerShell.

## <a name="install-azure-powershell"></a>Установите Azure PowerShell

Сначала установите последнюю версию модуля Azure PowerShell. Сведения о последнем выпуске см. в [заметках о выпуске](./release-notes-azureps.md).

1. [Установите Azure PowerShell](install-azurerm-ps.md).

2. Чтобы проверить установку, выполните `Get-Module AzureRM -ListAvailable` в командной строке.

## <a name="log-in-to-azure"></a>Вход в Azure

Войдите в интерактивном режиме:

1. Введите `Login-AzureRmAccount`. Появится диалоговое окно с запросом на ввод учетных данных Azure. С помощью параметра -EnvironmentName можно войти в Azure для Китая или Azure для Германии.

   Пример: Login-AzureRmAccount -EnvironmentName AzureChinaCloud

2. Введите электронный адрес и пароль, связанные с вашей учетной записью. Azure выполняет проверку подлинности и сохраняет учетные данные, а затем закрывает окно.

После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для доступа к ресурсам в подписке и управления ими.

## <a name="create-a-resource-group"></a>Создание группы ресурсов

Теперь, когда все настроено, вы можете создавать ресурсы в Azure с помощью Azure PowerShell.

Сначала создайте группу ресурсов. Группы ресурсов в Azure позволяют управлять разными ресурсами, которые вы хотите логически сгруппировать. Например, вы можете создать группу ресурсов для приложения или проекта, а затем добавить в эту группу виртуальную машину, базу данных и службу CDN.

Создайте группу ресурсов с именем MyResourceGroup в регионе Azure "Западная Европа". Используйте для этого следующую команду:

```powershell
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a>Создание виртуальной машины Windows

Теперь, когда у вас есть группа ресурсов, создайте в ней виртуальную машину Windows. Чтобы создать виртуальную машину, сначала нужно создать необходимые ресурсы и назначить их в качестве конфигурации. Затем эту конфигурацию можно использовать для создания виртуальной машины.

### <a name="create-the-required-network-resources"></a>Создание необходимых сетевых ресурсов

Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети. Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине. Создайте группу безопасности сети для защиты доступа к общедоступному адресу. Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.

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

### <a name="create-the-virtual-machine"></a>Создание виртуальной машины

Сначала укажите учетные данные для операционной системы.

```powershell
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

Теперь, когда у вас есть необходимые ресурсы, можно создать виртуальную машину. На этом шаге создайте объект конфигурации виртуальной машины. Потом эту конфигурацию можно использовать для создания виртуальной машины.

```powershell
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Команда `New-AzureRmVM` выводит результаты, когда виртуальная машина создана и готова к использованию.

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

Теперь войдите на созданную виртуальную машину Windows Server, используя протокол RDP и общедоступный IP-адрес этой виртуальной машины. Следующая команда отображает общедоступный IP-адрес, созданный в предыдущем скрипте.

```powershell
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

Если вы работаете на компьютере Windows, вы можете отобразить IP-адрес, выполнив команду mstsc в командной строке:

```powershell
mstsc /v:xx.xxx.xx.xxx
```

Для входа укажите те же учетные данные (имя пользователя и пароль), которые вы использовали при создании виртуальной машины.

## <a name="create-a-linux-virtual-machine"></a>Создание виртуальной машины Linux

Чтобы создать виртуальную машину Linux, сначала нужно создать необходимые ресурсы и назначить их в качестве конфигурации. Затем эту конфигурацию можно использовать для создания виртуальной машины. Предполагается, что вы уже создали группу ресурсов, как описано в предыдущем разделе. Кроме того, вам потребуется открытый ключ SSH `id_rsa.pub` в каталоге формата SSH вашего профиля пользователя.

### <a name="create-the-required-network-resources"></a>Создание необходимых сетевых ресурсов

Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети. Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине. Создайте группу безопасности сети для защиты доступа к общедоступному адресу. Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.

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

### <a name="create-the-virtual-machine"></a>Создание виртуальной машины

Теперь, когда у вас есть необходимые ресурсы, можно создать виртуальную машину. На этом шаге создайте объект конфигурации виртуальной машины. Потом эту конфигурацию можно использовать для создания виртуальной машины.

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

Вы можете войти на созданную виртуальную машину Linux, используя SSH и общедоступный IP-адрес этой виртуальной машины:

```bash
ssh xx.xxx.xxx.xxx
```

```Output
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

```powershell
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Также для своей инфраструктуры вы можете создать новую частную виртуальную сеть, используя следующую команду:

```powershell
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Преимущество Azure и Azure PowerShell заключается в том, что их можно использовать для создания как облачной инфраструктуры, так и управляемых служб платформы. Управляемые службы платформы также можно объединять с инфраструктурой, создавая еще более мощные решения.

Например, используя Azure PowerShell, вы можете создать службу приложений Azure. Служба приложений Azure — это управляемая служба платформы, на которой можно размещать веб-приложения, не беспокоясь об инфраструктуре. Создав службу приложений Azure, вы можете создать два новых веб-приложения Azure с помощью следующих команд:

```powershell
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Отображение списка развернутых ресурсов

Чтобы вывести список ресурсов, работающих в Azure, используйте командлет `Get-AzureRmResource`. В следующем примере показаны ресурсы, входящие в созданную группу ресурсов.

```powershell
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
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

```powershell
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Вам будет предложено подтвердить удаление указанных ресурсов.

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Также можно удалить несколько ресурсов одновременно. Например, следующая команда удаляет всю группу ресурсов MyResourceGroup, связанную со всеми примерами в этом руководстве по началу работы. Эта команда удаляет группу ресурсов и все ресурсы, которые группа содержит.

```powershell
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
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
