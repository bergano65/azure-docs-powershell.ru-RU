---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: ea1a656222383428f7e951ce858ec94c3fdc979e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733292"
---
# New-AzureRmAnalysisServicesFirewallConfig

## КРАТКИй обзор
Создает новую конфигурацию брандмауэра служб Analysis Services 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService] [-FirewallRules] List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule> 
```

## NОПИСАНИЕ
New-AzureRmAnalysisServicesFirewallConfig создает новый объект конфигурации брандмауэра

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRules $rule1,$rule2
```

Создание конфигурации правила брандмауэра без включения службы Power BI.

## ПАРАМЕТРЫ

### -EnablePowerBIService
Флаг, указывающий, включена ли служба PowerBI

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallRules
Список правил брандмауэра

```yaml
Type: List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule>
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## ВХОДНЫЕ данные

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesFirewallConfig

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmAnalysisServicesFirewallConfig](./New-AzureRmAnalysisServicesFirewallConfig.md)
