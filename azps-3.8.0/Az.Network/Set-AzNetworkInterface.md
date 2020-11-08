---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066964"
---
# Set-AzNetworkInterface

## КРАТКИй обзор
Обновляет сетевой интерфейс.

## Максимальное

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Параметр **Set-AzNetworkInterface** обновляет сетевой интерфейс.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Настройка сетевого интерфейса
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

В этом примере осуществляется настройка сетевого интерфейса.
Первая команда получает сетевой интерфейс с именем NetworkInterface1 в группе ресурсов ResourceGroup1.
Вторая команда задает частный IP-адрес конфигурации IP.
Третья команда задает статический метод выделения для частного IP-адреса.
Четвертая команда задает тег в сетевом интерфейсе.
Пятая команда использует данные, хранящиеся в переменной $Nic, для задания сетевого интерфейса.

### Пример 2: изменение параметров DNS для сетевого интерфейса
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

Первая команда получает сетевой интерфейс с именем NetworkInterface1, который существует в рамках группы ресурсов ResourceGroup1. Вторая команда добавляет DNS-сервер 192.168.1.100 в этот интерфейс. Третья команда применяет эти изменения к сетевому интерфейсу. Чтобы удалить DNS-сервер, следуйте приведенным выше командам, но замените ". Добавить "с". Remove (удалить) во второй команде.

### Пример 3: включение IP-переадресации на сетевом интерфейсе
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

Первая команда возвращает существующий сетевой интерфейс с именем NetworkInterface1 и сохраняет его в переменной $nic. Вторая команда изменяет значение "перенаправление IP" на "истина". Наконец, третья команда применяет изменения к сетевому интерфейсу. Чтобы отключить переадресацию IP на сетевом интерфейсе, следуйте примеру примера, но не забудьте изменить вторую команду на "$nic. EnableIPForwarding = 0 ".

### Пример 4: изменение подсети сетевого интерфейса
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

Первая команда получает сетевой интерфейс NetworkInterface1 и сохраняет его в переменной $nic. Вторая команда возвращает виртуальную сеть, связанную с подсетью, с которой будет связан сетевой интерфейс. Вторая команда получает подсеть и сохраняет ее в переменной $subnet 2. Третья команда, связанная с основным частным IP-адресом сетевого интерфейса с новой подсетью. Наконец, последняя команда применит эти изменения к сетевому интерфейсу.
>[!NOTE] 
>Перед изменением подсети должны быть динамические IP-конфигурации. Если у вас есть статические IP-конфигурации, измените ее на Dynamic, прежде чем продолжить. 
>[!NOTE]
>Если у сетевого интерфейса есть несколько конфигураций IP-адресов, перед выполнением последней команды Set-AzNetworkInterface необходимо выполнить команду "вперед" для всех этих конфигураций IP-адресов. Это можно сделать с помощью команды "вперед", но заменить "0" на нужный номер. Если сетевой интерфейс имеет N конфигураций IP, должны существовать N-1 этих команд.

### Пример 5: связывание и отмена связи группы безопасности сети с сетевым интерфейсом
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

Первая команда возвращает существующий сетевой интерфейс с именем NetworkInterface1 и сохраняет его в переменной $nic. Вторая команда получает существующую сетевую группу безопасности с именем MyNSG и сохраняет ее в переменной $nsg. Третья команда назначает $nsg $nicу. Наконец, команда "вперед" применяет изменения сетевого интерфейса. Чтобы отменить связь сетевых групп безопасности с сетевым интерфейсом, просто замените $nsg в третьей команде $null.

## ПАРАМЕТРЫ

### -AsJob
Выполнить командлет в фоновом режиме

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
Указывает объект сетевого интерфейса, представляющий состояние, для которого должен быть установлен сетевой интерфейс.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterface

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSNetworkInterface

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
