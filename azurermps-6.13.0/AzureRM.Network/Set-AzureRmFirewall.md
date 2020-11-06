---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556611"
---
# Set-AzureRmFirewall

## КРАТКИй обзор
Сохранение измененного брандмауэра.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmFirewall** обновляет брандмауэр Azure.

## ИЛЛЮСТРИРУЮТ

### 1: обновление приоритета коллекции правил приложения брандмауэра
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

В этом примере обновляется приоритет существующей коллекции правил брандмауэра Azure.
Предполагается, что брандмауэр Azure "AzureFirewall" в группе ресурсов "RG" имеет коллекцию правил приложений с именем "ruleCollectionName", команды выше будут изменять приоритет этой коллекции правил и затем обновлять брандмауэр Azure. Без команды Set-AzureRmFirewall все операции, выполненные на локальном объекте $azFw, не отражаются на сервере.

### 2. Создание брандмауэра Azure и установка коллекции правил приложений позже
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

В этом примере брандмауэр создается в первую очередь без каких-либо коллекций правил приложений. После этого создается правило приложения и коллекция правил приложения, а затем объект Firewall изменяется в памяти, не влияя на реальную конфигурацию в облаке. Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzureRmFirewall.

## ПАРАМЕТРЫ

### -AsJob
Выполнить командлет в фоновом режиме

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

### -AzureFirewall
AzureFirewall

```yaml
Type: PSAzureFirewall
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### PSAzureFirewall
Параметр "AzureFirewall" принимает значение типа "PSAzureFirewall" из конвейера.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)

[New-AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)
