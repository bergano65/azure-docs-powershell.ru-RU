---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 2675c304913e16f6d62f7b1f9067a7e4280422bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963971"
---
# Set-AzFirewall

## SYNOPSIS
Сохранение измененного брандмауэра.

## СИНТАКСИС

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet set-AzFirewall** обновляется брандмауэр Azure.

## ПРИМЕРЫ

### 1. Обновление приоритета для коллекции правил брандмауэра
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

В этом примере обновляется приоритет существующего сбора правил брандмауэра Azure.
Предположим, что брандмауэр Azure "AzureFirewall" в группе ресурсов "rg" содержит коллекцию правил приложения "ruleCollectionName", команды выше изменят приоритет этого сбора правил и обновят брандмауэр Azure после этого. Без Set-AzFirewall команды все операции, выполняемые с локальным объектом $azFw, не отражаются на сервере.

### 2. Создание брандмауэра Azure и настройка коллекции правил приложения позднее
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

В этом примере сначала создается брандмауэр без коллекций правил приложений. После создания правила приложения и коллекции правил приложения объект брандмауэра в памяти будет изменен, не влияя на реальные настройки в облаке. Чтобы изменения отображались в облаке, Set-AzFirewall должны быть вызваны.

### 3. Обновление режима операции Intel с угрозами брандмауэра Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

Этот пример обновляет режим операции Threat Intel брандмауэра Azure "AzureFirewall" в группе ресурсов "rg".
Без Set-AzFirewall команды все операции, выполняемые с локальным объектом $azFw, не отражаются на сервере.

### 4. Поиск и выделение брандмауэра
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
В этом примере извлекает и сохраняет брандмауэр, а также поиск брандмауэра. Команда Deallocate удаляет запущенную службу, но сохраняет конфигурацию брандмауэра. Чтобы изменения отображались в облаке, Set-AzFirewall должны быть вызваны.
Если пользователь хочет снова запустить службу, в брандмауэре следует использовать метод "Выделить".
Новые IP-адреса VNet и Public IP должны быть в той же группе ресурсов, что и брандмауэр. Для отражения изменений в облаке необходимо также Set-AzFirewall.

### 5. Выделение с общедоступным IP-адресом управления для сценариев принудительного туннелинга
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
В этом примере брандмауэр с общедоступным IP-адресом и подсетью управления выделяется для сценариев принудительного туннелизации. VNet должна содержать подсеть AzureFirewallManagementSubnet.

### 6. Добавление обще доступного IP-адреса в брандмауэр Azure
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

В этом примере общедоступный IP-адрес azFwPublicIp1, присоединенный к брандмауэру.

### 7. Удаление общеугодного IP-адреса из брандмауэра Azure
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

В этом примере общедоступный IP-адрес azFwPublicIp1 будет отсоединен от брандмауэра.

### 8. Изменение общеуправленного IP-адреса в брандмауэре Azure
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

В этом примере общедоступный IP-адрес управления брандмауэра будет изменен на "AzFwMgmtPublicIp2".

### 9. Добавление конфигурации DNS в брандмауэр Azure
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

В этом примере конфигурации DNS-прокси и DNS Server подключены к брандмауэру.

### 10. Обновление назначения существующего правила в коллекции правил брандмауэра приложения
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

В этом примере обновляется назначение существующего правила в коллекции правил брандмауэра Azure. Это позволяет автоматически обновлять правила при динамическом изменении IP-адресов.

### 11. Разрешение active FTP в брандмауэре Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

В этом примере в брандмауэре разрешена активная FTP-возможность.

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

### -AzureFirewall
The AzureFirewall

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
Перед запуском cmdlet вам будет предложено подтвердить его.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
