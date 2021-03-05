---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 0afd299103f1595afd100a7e9a72c4045896419d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987703"
---
# Set-AzNetworkInterface

## SYNOPSIS
Обновляет сетевой интерфейс.

## СИНТАКСИС

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Шрифт **Set-AzNetworkInterface** обновляет сетевой интерфейс.

## ПРИМЕРЫ

### Пример 1. Настройка сетевого интерфейса
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

В этом примере настроен сетевой интерфейс.
Первая команда получает сетевой интерфейс NetworkInterface1 в группе ресурсов ResourceGroup1.
Вторая команда задает частный IP-адрес конфигурации IP-адреса.
Третья команда задает способ выделения частных IP-адресов статический.
Четвертая команда задает тег в сетевом интерфейсе.
Пятая команда использует данные из переменной $Nic для изменения сетевого интерфейса.

### Пример 2. Изменение параметров DNS в интерфейсе сети
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Первая команда получает сетевой интерфейс NetworkInterface1, который существует в группе ресурсов ResourceGroup1. Вторая команда добавляет в интерфейс DNS-сервер 192.168.1.100. Третья команда применяет эти изменения к сетевому интерфейсу. Чтобы удалить DNS-сервер, выполните указанные выше команды, но замените ". Добавить" с помощью ". Удалить" во второй команде.

### Пример 3. Включить переадваровку IP-адресов в сетевом интерфейсе
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Первая команда получает существующий сетевой интерфейс NetworkInterface1 и сохраняет его в переменной $nic. Вторая команда изменяет значение переадваровки IP-адресов на истина. Наконец, изменения в сетевом интерфейсе применяются третьей командой. Чтобы отключить переадваровку IP-адресов в сетевом интерфейсе, выполните пример, но обязательно измените вторую команду на "$nic. EnableIPForwarding = 0".

### Пример 4. Изменение подсети сетевого интерфейса
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Первая команда получает сетевой интерфейс NetworkInterface1 и сохраняет ее в переменной $nic. Вторая команда возвращает виртуальную сеть, связанную с подсетью, с которую будет связан сетевой интерфейс. Вторая команда получает подсеть и сохраняет ее в переменной $subnet 2. Третья команда, связанная с основным частным IP-адресом сетевого интерфейса, с новой подсетей. Наконец, эти изменения применены последней командой в сетевом интерфейсе.
>[!NOTE] 
>Для изменения подсети конфигурации IP-адресов должны быть динамическими. Если у вас есть статические конфигурации IP-адресов, перед началом процедуры измените его на динамический. 
>[!NOTE]
>Если в сетевом интерфейсе несколько конфигураций IP-адресов, для всех этих конфигураций необходимо выполнять конечную команду Set-AzNetworkInterface IP-адресов. Для этого можно использовать 12-ю команду, заменив "0" соответствующим номером. Если сетевой интерфейс имеет конфигурацию N IP, то N-1 из этих команд должны существовать.

### Пример 5. Связывать и диссоциировать группу безопасности сети с интерфейсом сети
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Первая команда получает существующий сетевой интерфейс NetworkInterface1 и сохраняет его в переменной $nic. Вторая команда получает существующую группу безопасности сети MyNSG и сохраняет ее в переменной $nsg сети. Третья команда назначает $nsg $nic. Наконец, с помощью этой команды изменения применяются к сетевому интерфейсу. Чтобы отменить группировку безопасности в сетевом интерфейсе, просто замените $nsg третьей командой на $null.

## PARAMETERS

### -AsJob
Запуск cmdlet в фоновом режиме

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

### -NetworkInterface
Определяет объект сетевого интерфейса, представляющий состояние, в котором должен быть установлен сетевой интерфейс.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSNetworkInterface

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
