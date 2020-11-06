---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: e94cc565c2f22134f6bd4092247fbfa1f5a98b8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561900"
---
# New-AzureRmVmss

## КРАТКИй обзор
Создает объект VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmVmss** создает набор масштабов виртуальных машин (VMSS) в Azure.
Этот командлет принимает объект **VirtualMachineScaleSet** в качестве входных данных.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание VMSS
```
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

В следующем сложном примере создается VMSS.
Первая команда создает группу ресурсов с указанным именем и расположением.
Вторая команда использует командлет **New-AzureRmStorageAccount** для создания учетной записи хранения.
Третья команда затем использует командлет **Get-AzureRmStorageAccount** для получения учетной записи хранения, созданной во второй команде, и сохраняет результат в переменной $STOAccount.
Пятая команда использует командлет **New-AzureRmVirtualNetworkSubnetConfig** для создания подсети и сохраняет результат в переменной с именем $SubNet.
Шестая команда использует командлет **New-AzureRmVirtualNetwork** для создания виртуальной сети и сохраняет результат в переменной с именем $VNet.
Седьмая команда использует **Get-AzureRmVirtualNetwork** для получения сведений о виртуальной сети, созданной в шестой команде, и сохраняет данные в переменной с именем $VNet.
В восьмом девятом — команда **New-AzureRmPublicIpAddress** и **Get-AzureRmPublicIpAddress** используется для создания и получения сведений об общедоступном IP-адресе.
Команды хранят данные в переменной с именем $PubIP.
Десятая команда использует командлет **New-AzureRmLoadBalancerFrontendIpConfig** для создания балансировщика интерфейсной балансировки нагрузки и сохраняет результат в переменной с именем $frontend.
Одиннадцатая команда использует **New-AzureRmLoadBalancerBackendAddressPoolConfig** для создания конфигурации пула адресов сервера и сохраняет результат в переменной с именем $BackendAddressPool.
Двенадцати команда использует **New-AzureRmLoadBalancerProbeConfig** для создания пробной проверки и сохраняет данные пробы в переменной с именем $Probe.
В команде thirteenth с помощью командлета **New-AzureRmLoadBalancerInboundNatPoolConfig** можно создать конфигурацию пула NAT для подсистемы балансировки нагрузки входящих сетевых адресов.
Команда fourteenth использует **New-AzureRmLoadBalancerRuleConfig** для создания конфигурации правила подсистемы балансировки нагрузки и сохраняет результат в переменной с именем $LBRule.
В команде пятнадцати используется командлет **New-AzureRmLoadBalancer** для создания подсистемы балансировки нагрузки и сохранения результата в переменной с именем $ActualLb.
В шестнадцатой команде используется **Get-AzureRmLoadBalancer** для получения сведений о подсистеме балансировки нагрузки, созданной в команде пятнадцати, и сохраняет данные в переменной с именем $ExpectedLb.
В команде Seventeenth используется командлет **New-AzureRmVmssIPConfig** для создания конфигурации IP VMSS и сохранения сведений в переменной с именем $IPCfg.
Команда восемнадцатым месяцами эксплуатации использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.
В команде XIX для создания VMSS используется командлет **New-AzureRmVmss** .

## ПАРАМЕТРЫ

### -ResourceGroupName
Указывает имя группы ресурсов для VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Указывает объект **VirtualMachineScaleSet** , СОДЕРЖАЩИЙ свойства VMSS, создаваемые этим командлетом.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
Указывает имя VMSS, создаваемого этим командлетом.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
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

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Этот командлет не создает никаких выходных данных.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[Remove-AzureRmVmss](./Remove-AzureRmVmss.md)

[Restarting-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[Start-AzureRmVmss](./Start-AzureRmVmss.md)

[Остановить-AzureRmVmss](./Stop-AzureRmVmss.md)

[Update-AzureRmVmss](./Update-AzureRmVmss.md)


