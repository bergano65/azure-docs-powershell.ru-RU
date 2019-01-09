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
# <a name="get-started-with-azure-powershell"></a>Начало работы с Azure PowerShell

Модуль Azure PowerShell предназначен для администрирования ресурсов Azure из командной строки, а также для создания скриптов автоматизации, которые работают с Azure Resource Manager. Его можно использовать в браузере с [Azure Cloud Shell](/azure/cloud-shell/overview), а также установить на локальном компьютере. В этой статье содержатся инструкции по началу работы с Azure PowerShell и объясняются основные принципы работы этого модуля.

## <a name="install-azure-powershell"></a>Установите Azure PowerShell

Сначала установите последнюю версию модуля Azure PowerShell. Сведения о последнем выпуске см. в [заметках о выпуске](./release-notes-azureps.md).

1. [Установите Azure PowerShell](install-az-ps.md).

2. Чтобы проверить установку, выполните `Get-InstalledModule Az -AllVersions` в командной строке.

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

Самый простой способ начать работу — [запустить службу Cloud Shell](/azure/cloud-shell/quickstart).

1. Запустите Cloud Shell с верхней панели навигации портала Azure.

   ![Значок оболочки](~/media/get-started-azureps/shell-icon.png)

2. Выберите нужную подписку и создайте учетную запись хранения.

   ![Создание учетной записи хранения](~/media/get-started-azureps/storage-prompt.png)

Когда хранилище будет создано, Cloud Shell откроет сеанс PowerShell в браузере.

![Использование Cloud Shell с PowerShell](~/media/get-started-azureps/cloud-powershell.png)

## <a name="sign-in-to-azure"></a>Вход в Azure

Войдите в интерактивном режиме:

1. Введите `Connect-AzAccount`. Аргумент `-Environment` позволяет выполнять аутентификацию для другого региона или облака. Например, чтобы подключиться к Azure для Китая:

    ```powershell-interactive
    Connect-AzAccount -Environment AzureChinaCloud
    ```

2. Вы получите токен, используемый на https://microsoft.com/devicelogin. Откройте эту страницу в браузере и введите токен, чтобы войти с учетными данными Azure и авторизовать Azure PowerShell. 

После входа в учетную запись Azure вы можете использовать командлеты Azure PowerShell для работы с ресурсами в подписке и управления ими. Дополнительные сведения о процессе входа и доступных методах проверки подлинности см. в статье [Sign in with Azure PowerShell](authenticate-azureps.md) (Вход с помощью Azure PowerShell).

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>Создание виртуальной машины Windows с помощью простых значений по умолчанию

У командлета `New-AzVM` упрощенный синтаксис, что облегчает создание виртуальной машины. Вам нужно указать только два значения параметров: имя виртуальной машины и учетные данные локального администратора виртуальной машины.

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

Может возникнуть вопрос, что при этом еще создается, а также как настроена виртуальная машина. Сначала посмотрим на наши группы ресурсов.

```azurepowershell-interactive
Get-AzResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

Группа ресурсов **cloud-shell-storage-westus** создается при первом использовании Cloud Shell. Группа ресурсов **SampleVM** создается командлетом `New-AzVM`.

Но какие же ресурсы созданы в этой новой группе ресурсов?

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

Давайте получим дополнительные сведения о виртуальной машине. В этом примере показано, как получить сведения об образе операционной системы, который используется для создания виртуальной машины.

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

## <a name="create-a-fully-configured-linux-virtual-machine"></a>Создание полностью настроенной виртуальной машины Linux

В предыдущем примере для создания виртуальной машины Windows используется упрощенный синтаксис и значения параметров по умолчанию. В этом примере мы предоставляем значения для всех параметров виртуальной машины.

### <a name="create-a-resource-group"></a>Создание группы ресурсов

В этом примере показано, как создать группу ресурсов. Группы ресурсов в Azure позволяют управлять разными ресурсами, которые вы хотите логически сгруппировать. Например, вы можете создать группу ресурсов для приложения или проекта, а затем добавить в эту группу виртуальную машину, базу данных и службу CDN.

Создайте группу ресурсов с именем MyResourceGroup в регионе Azure uswest2. Используйте для этого следующую команду:

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

Эта новая группа ресурсов будет использоваться для размещения всех ресурсов, необходимых для создаваемой виртуальной машины. Чтобы создать виртуальную машину Linux, сначала нужно создать необходимые ресурсы и включить их в конфигурацию. Затем эту конфигурацию можно использовать для создания виртуальной машины. Кроме того, вам потребуется открытый ключ SSH `id_rsa.pub` в каталоге `.ssh` вашего профиля пользователя.

#### <a name="create-the-required-network-resources"></a>Создание необходимых сетевых ресурсов

Сначала создайте конфигурацию подсети, которая будет использоваться для создания виртуальной сети. Также нужно создать общедоступный IP-адрес, чтобы можно было подключаться к этой виртуальной машине. Создайте группу безопасности сети для защиты доступа к общедоступному адресу. Наконец, создайте виртуальный сетевой адаптер, используя все предыдущие ресурсы.

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

### <a name="create-the-vm-configuration"></a>Создание конфигурации виртуальной машины

Теперь, когда у вас есть необходимые ресурсы, можно создать объект конфигурации виртуальной машины.

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

### <a name="create-the-virtual-machine"></a>Создание виртуальной машины

Теперь мы можем создать виртуальную машину, используя объект конфигурации.

```azurepowershell-interactive
New-AzVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Вы можете войти в созданную виртуальную машину Linux, используя SSH и общедоступный IP-адрес этой виртуальной машины:

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

## <a name="creating-other-resources-in-azure"></a>Создание других ресурсов в Azure

Вы узнали, как создавать группы ресурсов, а также виртуальные машины Linux и Windows Server. Но вы также можете создать в Azure много других ресурсов.

Например, чтобы создать подсистему балансировки нагрузки Azure, которую можно затем связать с новой виртуальной машиной, выполните следующую команду:

```azurepowershell-interactive
New-AzLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westus2
```

Также для своей инфраструктуры вы можете создать новую частную виртуальную сеть, используя следующую команду:

```azurepowershell-interactive
$subnetConfig = New-AzVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzVirtualNetwork -ResourceGroupName myResourceGroup -Location westus2 `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Преимущество Azure и Azure PowerShell заключается в том, что их можно использовать для создания как облачной инфраструктуры, так и управляемых служб платформы. Управляемые службы платформы также можно объединять с инфраструктурой, создавая еще более мощные решения.

Например, используя Azure PowerShell, вы можете создать службу приложений Azure. Служба приложений Azure — это управляемая служба платформы, на которой можно размещать веб-приложения, не беспокоясь об инфраструктуре. Создав службу приложений Azure, вы можете создать два новых веб-приложения Azure с помощью следующих команд:

```azurepowershell-interactive
# Get a UUID for creating the apps to avoid name conflicts
$guid = [System.Guid]::NewGuid().ToString()

# Create an Azure AppService that we can host any number of web apps within
New-AzAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westus2

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzWebApp -Name MyWebApp-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
New-AzWebApp -Name MyWebApp2-$guid -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westus2
```

## <a name="listing-deployed-resources"></a>Отображение списка развернутых ресурсов

Чтобы вывести список ресурсов, работающих в Azure, используйте командлет `Get-AzResource`. В следующем примере показаны созданные ресурсы в новой группе ресурсов.

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

## <a name="deleting-resources"></a>Удаление ресурсов

Чтобы очистить учетную запись Azure, необходимо удалить ресурсы, созданные в этом примере. Используйте командлеты `Remove-Az*` для удаления ресурсов, которые больше не нужны. Чтобы удалить виртуальную машину Windows, выполните следующую команду:

```azurepowershell-interactive
Remove-AzVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Вам будет предложено подтвердить удаление указанного ресурса.

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Также за один раз можно удалить несколько ресурсов. Например, следующая команда удаляет группу ресурсов MyResourceGroup, которую мы использовали во всех предыдущих примерах.
Все ресурсы в группе также будут удалены.

```azurepowershell-interactive
Remove-AzResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Задача может занять несколько минут, в зависимости от количества и типа ресурсов.

## <a name="get-samples"></a>Получение примеров

Дополнительные сведения о способах использования Azure PowerShell см. в примерах популярных сценариев для [виртуальных машин Linux](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [виртуальных машин Windows](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [веб-приложений](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) и [баз данных SQL](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).

## <a name="next-steps"></a>Дополнительная информация

* [Вход с помощью Azure PowerShell](authenticate-azureps.md)
* [Управление подписками Azure с помощью Azure PowerShell](manage-subscriptions-azureps.md)
* [Создание субъектов-служб в Azure с помощью Azure PowerShell](create-azure-service-principal-azureps.md)
* Помощь от сообщества:
  * [Форум Azure на MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
