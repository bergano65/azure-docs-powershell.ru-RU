---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734619"
---
# Get-AzureRmFirewall

## КРАТКИй обзор
Получает брандмауэр Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmFirewall** получает один или несколько брандмауэров в группе ресурсов.

## ИЛЛЮСТРИРУЮТ

### 1: получение всех брандмауэров в группе ресурсов
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

В этом примере извлекаются все брандмауэры в группе ресурсов "rgName".

### 2. Загрузка брандмауэра по имени
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

В этом примере извлекается брандмауэр с именем "azFw" в группе ресурсов "rgName".

### 3. получение доступа к брандмауэру и Добавление набора правил приложения в брандмауэр
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

В этом примере извлекается брандмауэр, после чего в брандмауэр добавляется коллекция правил приложений, вызывая метод AddApplicationRuleCollection.

### 4. Извлеките брандмауэр и добавьте в брандмауэр коллекцию сетевых правил.
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

В этом примере извлекается брандмауэр, после чего в брандмауэр добавляется коллекция сетевых правил, вызывая метод AddNetworkRuleCollection.

### 5. Извлеките брандмауэр и выберите в контекстном меню набор правил приложения, используя имя из брандмауэра.
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

В этом примере извлекается брандмауэр и затем получается коллекция правил по имени, вызывающему метод GetApplicationRuleCollectionByName для объекта Firewall. Имя набора правил для метода GetApplicationRuleCollectionByName не учитывает регистр.

### 6. Извлеките брандмауэр и выберите в списке Сетевое правило по имени из брандмауэра.
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

В этом примере извлекается брандмауэр и затем получается коллекция правил по имени, вызывающему метод GetNetworkRuleCollectionByName для объекта Firewall. Имя набора правил для метода GetNetworkRuleCollectionByName не учитывает регистр.

### 7. получение брандмауэра и удаление набора правил приложения по имени из брандмауэра
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

В этом примере извлекается брандмауэр, после чего коллекция правил удаляется по имени, вызывая метод RemoveApplicationRuleCollectionByName для объекта Firewall. Имя набора правил для метода RemoveApplicationRuleCollectionByName не учитывает регистр.

### 8. получение брандмауэра и удаление из него семейства сетевых правил по имени из брандмауэра.
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

В этом примере извлекается брандмауэр, после чего коллекция правил удаляется по имени, вызывая метод RemoveNetworkRuleCollectionByName для объекта Firewall. Имя набора правил для метода RemoveNetworkRuleCollectionByName не учитывает регистр.

### 9: получение брандмауэра и его выделение
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

В этом примере извлекается брандмауэр и вызываются функции выделения ресурсов в брандмауэре, чтобы запустить службу брандмауэра с помощью конфигурации (коллекций приложений и сетевых правил), связанных с брандмауэром.

## ПАРАМЕТРЫ

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

### -Name (имя)
Указывает имя брандмауэра, который получает этот командлет.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Указывает имя группы ресурсов, к которой относится брандмауэр.

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

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Этот командлет не поддерживает никаких входных данных.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
