---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 36ba29104fbc9e87ae2776504dc48bed8a5b9ffa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065801"
---
# Set-AzFirewall

## КРАТКИй обзор
Сохранение измененного брандмауэра.

## Максимальное

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzFirewall** обновляет брандмауэр Azure.

## ИЛЛЮСТРИРУЮТ

### 1: обновление приоритета коллекции правил приложения брандмауэра
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

В этом примере обновляется приоритет существующей коллекции правил брандмауэра Azure.
Предполагается, что брандмауэр Azure "AzureFirewall" в группе ресурсов "RG" имеет коллекцию правил приложений с именем "ruleCollectionName", команды выше будут изменять приоритет этой коллекции правил и затем обновлять брандмауэр Azure. Без команды Set-AzFirewall все операции, выполненные на локальном объекте $azFw, не отражаются на сервере.

### 2. Создание брандмауэра Azure и установка коллекции правил приложений позже
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

В этом примере брандмауэр создается в первую очередь без каких-либо коллекций правил приложений. После этого создается правило приложения и коллекция правил приложения, а затем объект Firewall изменяется в памяти, не влияя на реальную конфигурацию в облаке. Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzFirewall.

### 3: обновление угрозы в режиме функционирования Intel в брандмауэре Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

В этом примере обновляется режим функционирования программного кода Intel для брандмауэра Azure "AzureFirewall" в группе ресурсов "RG".
Без команды Set-AzFirewall все операции, выполненные на локальном объекте $azFw, не отражаются на сервере.

### 4. выделять и выделять брандмауэр
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
В этом примере извлекается брандмауэр, размещается брандмауэр и сохраняется. Команда "освободить" удаляет запущенную службу, но сохраняет конфигурацию брандмауэра. Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzFirewall.
Если пользователь хочет снова запустить службу, необходимо вызвать метод выделения на брандмауэре.
Новая виртуальная сеть и общедоступный IP-адрес должны находиться в той же группе ресурсов, что и брандмауэр. Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzFirewall.

### 5. выделять с общедоступным IP-адресом для управления сценариями принудительного туннелирования
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress - ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
Этот пример выделяет брандмауэр с общедоступным IP-адресом управления и подсетью для сценариев принудительного туннелирования. VNet должен содержать подсеть с именем "AzureFirewallManagementSubnet".

### 6. Добавьте общедоступный IP-адрес в брандмауэр Azure.
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

В данном примере — общедоступный IP-адрес "azFwPublicIp1", подключенный к межсетевому экрану.

### 7. Удаление общедоступного IP-адреса из брандмауэра Azure
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

В этом примере общедоступный IP-адрес "azFwPublicIp1" отделен от брандмауэра.

### 8: изменение общедоступного IP-адреса для управления в брандмауэре Azure
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

В этом примере общедоступный IP-адрес управления для вашего брандмауэра изменится на "AzFwMgmtPublicIp2".


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

### -AzureFirewall
AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Confirm
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
