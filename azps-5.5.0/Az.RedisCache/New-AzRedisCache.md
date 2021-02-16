---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217865"
---
# New-AzRedisCache

## SYNOPSIS
Создает кэш Redis.

## СИНТАКСИС

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для **создания кэша Azure Redis создается cmdlet New-AzRedisCache.**

## ПРИМЕРЫ

### Пример 1. Создание кэша Redis
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Эта команда создает кэш Redis.

### Пример 2. Создание стандартного кэша redis SKU
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]} 
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Эта команда создает кэш Redis.

## PARAMETERS

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

### -EnableNonSslPort
Указывает, включен ли порт, не sSL.
Значение по умолчанию — $False (не SSL-порт отключен).

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Определяет место, в котором нужно создать кэш Redis.
Допустимые значения: 
- Северный Центр США
- Южный Центр США
- Центральная часть США
- Западная Европа
- Северная Европа
- Запад США
- Восток США
- Восток США 2
- Восточная Япония
- Западная Япония
- Южная Бразилия
- Юго-Восточная Азия
- Восточная Азия
- Восточная Австралия
- Юго-Восточная Австралия

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MinimumTlsVersion
Укажите версию TLS, необходимую для подключения клиентов к кэше.

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

### -Name
Имя кэша Redis, который нужно создать.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RedisConfiguration
Определяет параметры конфигурации Redis.
Допустимыми значениями для этого параметра являются:
- RDB-резервное копирование.
Указывает, что сохранение данных Redis включено.
Только премиум-уровень.
- rdb-storage-connection-string.
Указывает строку подключения к учетной записи хранения для сохранения данных Redis.
Только премиум-уровень.
- частота rdb-резервного копирования.
Определяет частоту резервного копирования для сохранения данных Redis.
Только премиум-уровень. 
- maxmemory-reserved.
Настраивает память, зарезервированную для процессов, не кэшируемых.
Стандартные и премиум-уровни. 
- maxmemory-policy.
Настраивает политику присоединения к кэшу.
Все уровни цен. 
- notify-keyspace-events.
Настраивает уведомления в области клавиш.
Стандартные и премиум-уровни. 
- hash-max-ziplist-entries.
Оптимизация памяти для небольших типов агрегированных данных.
Стандартные и премиум-уровни. 
- hash-max-ziplist-value.
Оптимизация памяти для небольших типов агрегированных данных.
Стандартные и премиум-уровни. 
- set-max-intset-entries.
Оптимизация памяти для небольших типов агрегированных данных.
Стандартные и премиум-уровни. 
- zset-max-ziplist-entries.
Оптимизация памяти для небольших типов агрегированных данных.
Стандартные и премиум-уровни. 
- zset-max-ziplist-value.
Оптимизация памяти для небольших типов агрегированных данных.
Стандартные и премиум-уровни. 
- базы данных.
Количество баз данных.
Это свойство можно настроить только при создании кэша.
Стандартные и премиум-уровни.
Дополнительные сведения см. в кэше Azure Redis с помощью Azure http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) PowerShell.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов, в которой нужно создать кэш Redis.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ShardCount
Определяет количество шардаков, которые нужно создать в кэше кластера Premium.
Допустимыми значениями для этого параметра являются:
- 1
- 2
- 3
- 4
- 5
- 6
- 7
- 8
- 9 
- 10

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
Определяет размер кэша Redis.
Допустимые значения: 
- P1
- P2
- P3
- P4
- P5
- C0
- C1
- C2
- C3
- C4
- C5
- C6
- 250 МБ
- 1 ГБ
- 2,5 ГБ
- 6 ГБ
- 13 ГБ
- 26 ГБ
- По умолчанию 53 ГБ — 1 ГБ или C1.

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

### -SKU
Определяет SKU кэша Redis, который нужно создать.
Допустимые значения: 
- Базовая
- Стандартный
- Premium Значение по умолчанию — "Стандартная".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StaticIP
Указывает уникальный IP-адрес в подсети для кэша Redis.
Если значение для этого параметра не задано, этот cmdlet выбирает IP-адрес из подсети.

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

### -Tag
Hash table which represents tags.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
Этот параметр был неподготовлен.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Список зон.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### System.Collections.Hashtable

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String[]

## OUTPUTS

### Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzRedisCache](./Get-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)

[Set-AzRedisCache](./Set-AzRedisCache.md)


