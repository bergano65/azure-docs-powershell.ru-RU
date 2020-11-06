---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 231787f57061ff4e118510c3dc166915b39da436
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563380"
---
# Get-AzureRmRedisCacheFirewallRule

## КРАТКИй обзор
Получение правил брандмауэра, заданных для кэша Redis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Если параметр **RuleName** задан, командлет **Get-AzureRmRedisCacheFirewallRule** получает подробные сведения о указанном правиле брандмауэра для кэша Redis Azure. Если задано только **имя** , эта операция получает все правила брандмауэра, доступные в этом кэше Redis.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение отдельного правила брандмауэра
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

Эта команда получает правило брандмауэра с именем ruleone из кэша Redis с именем mycache.

### Пример 2: получение всех правил брандмауэра
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

Эта команда получает все правила брандмауэра из кэша Redis с именем mycache.

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
Имя кэша Redis.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, в которой находится кэш.

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

### -RuleName
Имя правила брандмауэра.

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

### System. String
Вы можете передавать входные данные командлету по имени, но не по значению.

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisFirewallRule, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmRedisCacheFirewallRule](./New-AzureRmRedisCacheFirewallRule.md)

[Remove-AzureRmRedisCacheFirewallRule](./Remove-AzureRmRedisCacheFirewallRule.md)

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[New-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)
