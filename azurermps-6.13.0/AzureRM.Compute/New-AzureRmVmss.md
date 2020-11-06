---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: 9f6135917f2e6cbfc05511637b3b20bd126d54b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556783"
---
# New-AzureRmVmss

## КРАТКИй обзор
Создает объект VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### DefaultParameter (по умолчанию)
```
New-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
```
New-AzureRmVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmVmss** создает набор масштабов виртуальных машин (VMSS) в Azure.
Используйте простой набор параметров ( `SimpleParameterSet` ), чтобы быстро создать предварительно заданные VMSS и связанные ресурсы. Используйте набор параметров по умолчанию ( `DefaultParameter` ) для более сложных сценариев, если вам нужно точно настроить каждый компонент VMSS и каждый связанный ресурс перед его созданием.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание VMSS с помощью **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzureRmVmss -Credential $vmCred -VMScaleSetName $vmssName
```

В приведенной выше команде создаются следующие элементы с именем `$vmssName` :
* Группа ресурсов
* Виртуальная сеть
* Подсистема балансировки нагрузки
* Общедоступный IP-адрес
* VMSS с 2 экземплярами

Изображение по умолчанию, выбранное для виртуальных машин в VMSS, `2016-Datacenter Windows Server` и SKU `Standard_DS1_v2`

### Пример 2: создание VMSS с помощью **`DefaultParameterSet`**
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

В сложном примере выше создается VMSS, а далее показано, что происходит:
* Первая команда создает группу ресурсов с указанным именем и расположением.
* Вторая команда использует командлет **New-AzureRmStorageAccount** для создания учетной записи хранения.
* Третья команда затем использует командлет **Get-AzureRmStorageAccount** для получения учетной записи хранения, созданной во второй команде, и сохраняет результат в переменной $STOAccount.
* Пятая команда использует командлет **New-AzureRmVirtualNetworkSubnetConfig** для создания подсети и сохраняет результат в переменной с именем $SubNet.
* Шестая команда использует командлет **New-AzureRmVirtualNetwork** для создания виртуальной сети и сохраняет результат в переменной с именем $VNet.
* Седьмая команда использует **Get-AzureRmVirtualNetwork** для получения сведений о виртуальной сети, созданной в шестой команде, и сохраняет данные в переменной с именем $VNet.
* В восьмом девятом — команда **New-AzureRmPublicIpAddress** и **Get-AzureRmPublicIpAddress** используется для создания и получения сведений об общедоступном IP-адресе.
* Команды хранят данные в переменной с именем $PubIP.
* Десятая команда использует командлет **New-AzureRmLoadBalancerFrontendIpConfig** для создания балансировщика интерфейсной балансировки нагрузки и сохраняет результат в переменной с именем $frontend.
* Одиннадцатая команда использует **New-AzureRmLoadBalancerBackendAddressPoolConfig** для создания конфигурации пула адресов сервера и сохраняет результат в переменной с именем $BackendAddressPool.
* Двенадцати команда использует **New-AzureRmLoadBalancerProbeConfig** для создания пробной проверки и сохраняет данные пробы в переменной с именем $Probe.
* В команде thirteenth с помощью командлета **New-AzureRmLoadBalancerInboundNatPoolConfig** можно создать конфигурацию пула NAT для подсистемы балансировки нагрузки входящих сетевых адресов.
* Команда fourteenth использует **New-AzureRmLoadBalancerRuleConfig** для создания конфигурации правила подсистемы балансировки нагрузки и сохраняет результат в переменной с именем $LBRule.
* В команде пятнадцати используется командлет **New-AzureRmLoadBalancer** для создания подсистемы балансировки нагрузки и сохранения результата в переменной с именем $ActualLb.
* В шестнадцатой команде используется **Get-AzureRmLoadBalancer** для получения сведений о подсистеме балансировки нагрузки, созданной в команде пятнадцати, и сохраняет данные в переменной с именем $ExpectedLb.
* В команде Seventeenth используется командлет **New-AzureRmVmssIPConfig** для создания конфигурации IP VMSS и сохранения сведений в переменной с именем $IPCfg.
* Команда восемнадцатым месяцами эксплуатации использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.
* В команде XIX для создания VMSS используется командлет **New-AzureRmVmss** .

## ПАРАМЕТРЫ

### -AllocationMethod
Метод выделения для общедоступного IP-адреса набора шкал (static или Dynamic).  Если значение не указано, выделение будет статическим.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPoolName
Имя пула адресных адресов серверной платформы, который будет использоваться в подсистеме балансировки нагрузки для этого набора масштабов.  Если значение не задано, будет создана новая группа серверной базы данных с тем же именем, что и в наборе масштабов.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPort
Номера внутренних портов, используемые подсистемой балансировки нагрузки для связи с виртуальными машинами в установленном масштабе.  Если значения не указаны, для виртуальных компьютеров Windows будут использоваться порты 3389 и 5985, а для виртуальных машин Linux будет использоваться порт 22.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Учетные данные администратора (имя пользователя и пароль) для виртуальных машин в этом множестве масштабов.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataDiskSizeInGb
Задает размеры дисков данных в ГБ.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
Метка доменного имени для общедоступного доменного имени Fully-Qualified (FQDN) для данного множества масштабов. Это первый компонент доменного имени, которое автоматически назначается набору масштабов. Автоматически назначаемые доменные имена используют форму ( <DomainNameLabel> ..). <Location> cloudapp.azure.com). Если значение не задано, по умолчанию будет использоваться метка доменного имени для объединения <ScaleSetName> и <ResourceGroupName> .

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontendPoolName
Имя пула адресных интерфейсов, который будет использоваться в подсистеме балансировки нагрузки для набора масштабов.  Если значение не задано, будет создан новый пул адресных веб-интерфейсов с тем же именем, что и в наборе масштабов.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
Имя образа для виртуальных машин в этом наборе масштабов. Если значение не указано, будет использоваться изображение "центр обработки данных Windows Server 2016".

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceCount
Количество образов виртуальных машин в наборе масштабов.  Если значение не задано, будет создано 2 экземпляра.

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerName
Имя подсистемы балансировки нагрузки, используемой с этим набором масштабов.  Если значение не задано, будет создаваться новая служба подсистемы балансировки нагрузки с тем же именем, что и набор масштабирования.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Место Azure, в котором будет создан этот параметр масштабирования.  Если значение не задано, расположение будет выводиться из расположения других ресурсов, указанных в параметрах.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NatBackendPort
Внутренний порт для преобразования входящего сетевого адреса.

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
Имя общедоступного IP-адреса для использования с этим набором масштабов.  Новый общедоступный IP-адрес с тем же именем, что и у множества масштабирования, будет создан, если значение не указано.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов для VMSS.  Если значение не задано, будет создана новая группа ресурсов с тем же именем, что и у множества.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecurityGroupName
Имя группы безопасности сети, применяемой к этому набору масштабов.  Если значение не задано, будет создана группа безопасности сети по умолчанию с тем же именем, что и в наборе масштабов.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SinglePlacementGroup
Используйте этот параметр, чтобы создать набор масштабов в одной группе размещения, по умолчанию — по нескольким группам.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
Префикс адреса подсети, используемой этим набором элементов масштабирования. Параметры подсети по умолчанию (192.168.1.0/24) будут применены, если не задано значение.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Имя подсети, используемой в этом наборе масштабов.  Новая подсеть будет создана с тем же именем, что и в наборе масштабирования, если значение не указано.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemAssignedIdentity
Если параметр присутствует, ВМ (-ы) в наборе Scale (—) назначается (-а) управляемому системному удостоверению, которое создается автоматически.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePolicyMode
Режим политики обновления для экземпляров виртуальных машин в этом множестве масштабов.  Политика обновления может определять автоматические, ручные и чередующиеся обновления.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAssignedIdentity
Имя удостоверения управляемой службы, которое должно быть назначено для ВМ (ов) в наборе масштабов.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Указывает объект **VirtualMachineScaleSet** , СОДЕРЖАЩИЙ свойства VMSS, создаваемые этим командлетом.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VirtualNetworkName
Имя виртуальной сети, используемой в этом множестве масштабов.  Если значение не задано, будет создана новая виртуальная сеть с тем же именем, что и у множества.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMScaleSetName
Указывает имя VMSS, создаваемого этим командлетом.

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Размер экземпляров виртуальных машин в этом наборе масштабов.  Если размер не указан, будет использоваться размер по умолчанию (Standard_DS1_v2).

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -VnetAddressPrefix
Префикс адреса для виртуальной сети, используемой в этом множестве масштабов.  Значения префиксов виртуальных сетевых адресов по умолчанию (192.168.0.0/16) будут использоваться, если не задано значение.

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -Zone
Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet
Параметры: VirtualMachineScaleSet (ByValue)

### System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restarting-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Остановить-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


