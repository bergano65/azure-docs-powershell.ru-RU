---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732420"
---
# New-AzureRmRedisCache

## КРАТКИй обзор
Создание кэша Redis.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmRedisCache** создает кэш Redis Azure.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание кэша Redis
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


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
```

Эта команда создает кэш Redis.

### Пример 2: создание стандартного кэша Redis для SKU
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


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
```

Эта команда создает кэш Redis или обновляет кэш Redis, если он уже существует.

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

### -Location
Указывает место для создания кэша Redis.
Допустимые значения: 

- Северный Центральный США
- Южная Центральная американская
- Центральная американская
- Западная Европа
- Северная Европа
- Западная часть США
- Восточная часть США
- Восточная часть 2
- Восточная Япония
- Западная часть Японии
- Южная Бразилия
- Юго-Восточная Азия
- Восточная Азия
- Восточная Австралия
- Юго-восток Австралии

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
Указывает имя создаваемого кэша Redis.

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

### -RedisVersion
Этот параметр устарел и будет удален из будущих выпусков.

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

### -ResourceGroupName
Указывает имя группы ресурсов, в которой нужно создать кэш Redis.

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
Для этого параметра допустимы следующие значения:

- 1,1
- 2
- Трехконтактный
- четырехпроцессорном
- 5
- 152
- 5-7
- No8
- @ 
- 5-10

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

### -StaticIP
Задает уникальный IP-адрес в подсети для кэша Redis.

Если вы не укажете значение для этого параметра, этот командлет выберет IP-адрес из подсети.

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

### -Подсеть
Указывает имя подсети для развертывания кэша Redis.

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

### -VirtualNetwork
Указывает ИД виртуальной сети, в которой развертывается кэш Redis.

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
Вы можете передавать входные данные командлету по имени, но не по значению.

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. RedisCache. Models. RedisCacheAttributesWithAccessKeys
Этот командлет возвращает все атрибуты кэша Redis, включая первичные и вторичные ключи доступа.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


