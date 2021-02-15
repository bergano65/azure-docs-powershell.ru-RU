---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: e2ca08746ab9b4dc2ef2265a59cdab00ac42cf33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211713"
---
# New-AzVmssIpConfig

## SYNOPSIS
Создает конфигурацию IP-адреса для сетевого интерфейса VMSS.

## СИНТАКСИС

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet New-AzVmssIpConfig** создается объект конфигурации IP-адреса для сетевого интерфейса набора виртуальных машин (VMSS).
Укажите конфигурацию из этого cmdlet в качестве параметра *IPConfiguration* для Add-AzVmssNetworkInterfaceConfiguration.

## ПРИМЕРЫ

### Пример 1. Создание объекта конфигурации IP для интерфейса VMSS
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Эта команда создает объект конфигурации IP-адреса с именем ContosoVmssInterface02.
Для этой команды используется ранее определенный ИД подсети, который хранится в $SubnetId.
Команда сохраняет параметры конфигурации в переменной $IPConfiguration для использования с **Add-AzVmssNetworkInterfaceConfiguration.**

### Пример 2. Создание объекта конфигурации IP-адреса, который содержит параметры пула NAT
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Эта команда создает объект конфигурации IP-адреса с именем ContosoVmssInterface03, а затем сохраняет его в переменной $IPConfiguration для использования в дальнейшем.
Для этой команды используется ранее определенный ИД подсети, который хранится в $SubnetId.
Команда сохраняет параметры конфигурации в переменной $IPConfiguration для использования в дальнейшем.
Команда определяет значения параметров *LoadBalancerInboundNatPoolsId* и *LoadBalancerBackendAddressPoolsId.*

## PARAMETERS

### -ApplicationGatewayBackendAddressPoolsId
Указывает массив ссылок, которые нужно объединить с пулами адресов нагрузки.
Такой набор может ссылаться на пул адресов внутреннего и внутреннего пула общедоступных адресов.
В нескольких наборах нельзя использовать один и тот же баланс загрузки.

```yaml
Type: System.String[]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSetting
Параметры DNS, которые будут применяться к общедоступным IP-адресам.
Метка доменного имени, которая будет применена к параметрам DNS на общедоступных IP-адресах.
Совмещение метки доменного имени и индекса vm будет меткой доменного имени для ресурсов, которые будут созданы для общедоступных IP-адресов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Id
Определяет ИД.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IpTag
Определяет массив объектов IP-тегов.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Указывает массив ссылок на пулы сетевых адресов (NAT) для пулов балансиры нагрузки.
Набор масштаба может ссылаться на входящие пулы NAT одного открытого и одного внутреннего балансиров нагрузки.
В нескольких наборах нельзя использовать один и тот же баланс загрузки.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerInboundNatPoolsId
Указывает массив ссылок на входящие пулы NAT для балансиваров нагрузки.
Набор масштаба может ссылаться на входящие пулы NAT одного открытого и одного внутреннего балансиров нагрузки.
В нескольких наборах нельзя использовать один и тот же баланс загрузки.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Указывает имя конфигурации IP-адреса.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Primary
Указывает основную конфигурацию IP-адреса, если сетевой интерфейс имеет несколько конфигураций IP-адресов.

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

### -PrivateIPAddressVersion
Укажите конфигурацию IP-адреса для личного IP-адреса.  Значение по умолчанию — IPv4.  Возможные значения: IPv4 и IPv6.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressConfigurationIdleTimeoutInMinutes
Время ожидания неав то же самое для общего IP-адреса.

```yaml
Type: System.Int32
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
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPAddressVersion
Укажите конфигурацию IP-адреса для общего IP-адреса.  Значение по умолчанию — IPv4.  Возможные значения: IPv4 и IPv6.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicIPPrefix
ID of Public IP Prefix (Префикс общего IP-адреса)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Определяет ИД подсети, в которой создается сетевой интерфейс VMSS в конфигурации.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.String[]

### System.Int32

### Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetIpTag[]

## OUTPUTS

### Microsoft.Azure.Management.Compute.Models.VirtualMa modelseScaleSetIPConfiguration

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Add-AzVmssNetworkInterfaceConfiguration](./Add-AzVmssNetworkInterfaceConfiguration.md)


