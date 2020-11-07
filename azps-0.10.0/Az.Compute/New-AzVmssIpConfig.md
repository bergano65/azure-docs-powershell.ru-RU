---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 41b176d5952e9a33d0d0868b97fc71a14d6b43d8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911451"
---
# New-AzVmssIpConfig

## КРАТКИй обзор
Создание IP-конфигурации для сетевого интерфейса VMSS.

## Максимальное

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzVmssIpConfig** создает объект конфигурации IP для сетевого интерфейса набора масштабирования виртуальных машин (VMSS).
Укажите конфигурацию из этого командлета в качестве параметра *IP* для командлета Add-AzVmssNetworkInterfaceConfiguration.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание объекта конфигурации IP для интерфейса VMSS
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Эта команда создает объект конфигурации IP с именем ContosoVmssInterface02.
В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.
Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования с помощью **Add-AzVmssNetworkInterfaceConfiguration**.

### Пример 2: создание объекта конфигурации IP, включающего параметры пула NAT
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Эта команда создает объект конфигурации IP с именем ContosoVmssInterface03 и сохраняет его в переменной $IPConfiguration для последующего использования.
В команде используется ранее определенный идентификатор подсети, хранящийся в $SubnetId.
Команда сохраняет параметры конфигурации в переменной $IPConfiguration для последующего использования.
Команда задает значения для параметров *LoadBalancerInboundNatPoolsId* и *LoadBalancerBackendAddressPoolsId* .

## ПАРАМЕТРЫ

### -ApplicationGatewayBackendAddressPoolsId
Указывает массив ссылок на серверные пулы адресных пулов подсистем балансировки нагрузки.
Набор масштабов может ссылаться на пулы серверных адресов одного открытого и одного внутреннего подсистемы балансировки нагрузки.
Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSetting
Параметры DNS, применяемые к адресам publicIP.
Метка доменного имени параметров DNS, которые будут применяться к publicIP адресам.
Объединение метки доменного имени и индекса ВМ — это метки доменных имен ресурсов общедоступного IP-адреса, которые будут созданы.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Указывает идентификатор.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Задает массив ссылок на пулы NAT для подсистем балансировки нагрузки.
Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.
Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Указывает массив ссылок на входящие пулы NAT для подсистем балансировки нагрузки.
Набор масштабов может ссылаться на входящие пулы NAT для одной открытой и одной внутренней подсистемы балансировки нагрузки.
Несколько наборов масштабов не могут использовать одну и ту же подсистему балансировки нагрузки.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Указывает имя конфигурации IP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Primary
Определяет основную конфигурацию IP-адреса в случае, если сетевой интерфейс имеет несколько конфигураций IP.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateIPAddressVersion
Укажите IP-конфигурацию: либо IPv4, либо IPv6. По умолчанию используется протокол IPv4.  Возможные значения: "IPv4" и "IPv6".

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
Таймаут простоя общего IP-адреса.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationName
Имя конфигурации адреса publicIP.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Указывает идентификатор подсети, в котором конфигурация создает сетевой интерфейс VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. COMPUTE. Models. VirtualMachineScaleSetIPConfiguration

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


