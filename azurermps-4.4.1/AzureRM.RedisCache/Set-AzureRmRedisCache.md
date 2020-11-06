---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562235"
---
# Set-AzureRmRedisCache

## КРАТКИй обзор
Изменяет кэш Redis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzureRmRedisCache** изменяет кэш Azure Redis.

## ИЛЛЮСТРИРУЮТ

### Пример 1: изменение кэша Redis
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
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
```

Эта команда обновляет MaxMemory-политику для кэша Redis с именем MyCache.

## ПАРАМЕТРЫ

### -EnableNonSslPort
Указывает, включен ли порт без SSL.
Значение по умолчанию — $False (порт без SSL отключен).

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

### -MaxMemoryPolicy
Этот параметр устарел.
Для задания MaxMemory-Policy используйте параметр *RedisConfiguration* .
Например: 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### -Name (имя)
Указывает имя кэша Redis, который нужно обновить.

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
Задает параметры конфигурации Redis.
Для этого параметра допустимы следующие значения:

- RDB — включена резервная копия.
Указывает на то, что сохраняемость данных Redis включена.
Только уровень Premium.
- RDB — строка подключения к хранилищу.
Задает строку подключения к учетной записи хранения для Redis сохраняемости данных.
Только уровень Premium.
- RDB — периодичность резервного копирования.
Указывает периодичность резервного копирования для сохраняемости данных Redis.
Только уровень Premium. 
- MaxMemory — зарезервирован.
Настраивает память, зарезервированную для процессов без кэширования.
Уровни Standard и Premium. 
- MaxMemory — политика.
Настройка политики вытеснения для кэша.
Все ценовые категории. 
- Notify-keyspace-Events.
Настраивает уведомления keyspace.
Уровни Standard и Premium. 
- хэш-максимум-ziplist-записи.
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- hash-Max-ziplist-value.
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- Set-Max-intset-"записи".
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- zset-Max-ziplist-(записи).
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- zset-Max-ziplist-value.
Настройка оптимизации памяти для небольших типов данных агрегатов.
Уровни Standard и Premium. 
- баз данных.
Настраивает количество баз данных.
Это свойство можно настроить только при создании кэша.
Уровни Standard и Premium.

Дополнительные сведения можно найти в разделе Управление кэшем Redis Azure с помощью Azure PowerShell https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .

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
Указывает имя группы ресурсов, которая содержит кэш Redis.

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
Задает количество сегментов для создания в кэше высококачественных кластеров.

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
Задает размер кэша Redis.
Допустимые значения: 

- P1
- –
- –
- P4
- C0
- C1
- Режим
- Ячейку
- C4
- C5
- C6
- 250MB
- Гбайт
- 2,5 ГБ
- 6GB
- 13GB
- 26GB
- 53GB

Значение по умолчанию — 1 ГБ или C1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Указывает SKU кэша Redis для создания.
Допустимые значения: 

- Базового
- Стандартная
- Версию

По умолчанию используется значение Standard.

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

### -TenantSettings
Этот параметр устарел.

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

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего
Вы можете передавать входные данные командлету по имени свойства, но не по значению.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys
Возвращает все атрибуты кэша Redis, включая первичные и вторичные ключи доступа.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[New-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)


