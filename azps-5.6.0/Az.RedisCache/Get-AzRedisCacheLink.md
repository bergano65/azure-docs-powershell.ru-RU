---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 9b1957054c243de8776f0063e236f9e19980af54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982291"
---
# Get-AzRedisCacheLink

## SYNOPSIS
Получить ссылку на геокопию для Кэша Redis.

## СИНТАКСИС

### AllLinksForCache (по умолчанию)
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForPrimaryCache
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SingleLink
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForSecondaryCache
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Существует четыре разных способа получить подробные ссылки гео-репликации. Укайте имя параметра или PrimaryServerName и/или SecondaryServerName. После этого будет возвращена вся ссылка, в которой есть кэш. Если задано только имя PrimaryServerName, возвращаются все ссылки, для которых кэш является основным. Если задано только имя SecondaryServerName, возвращаются все ссылки, кэш которых является дополнительным. Если primaryServerName и SecondaryServerName both are given then specific link with correct role will be returned. 

## ПРИМЕРЫ

### Пример 1. Использование набора параметров AllLinksForCache
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Эта команда получает все ссылки гео-репликации для кэша Redis с именем mycache1.

### Пример 2. Использование набора параметров AllLinksForPrimaryCache
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Эта команда получает ссылки гео-репликации, где кэш Redis с именем mycache1 является основным.

### Пример 3. Использование набора параметров AllLinksForSecondaryCache
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Эта команда получает ссылки гео-репликации, где кэш Redis с именем mycache2 является дополнительным.

### Пример 4. Использование набора параметров SingleLink
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Эта команда получает одну ссылку гео-репликации, где кэш Redis с именем mycache1 является основным, а кэш Redis с именем mycache2 — дополнительным.

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

### -Name
Имя кэша redis.

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrimaryServerName
Имя основного кэша redis в ссылке.

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryServerName
Имя дополнительного кэша redis в ссылке.

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[New-AzRedisCacheLink](./New-AzRedisCacheLink.md)

[Remove-AzRedisCacheLink](./Remove-AzRedisCacheLink.md)

[Get-AzRedisCache](./Get-AzRedisCache.md)

[New-AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)

[Set-AzRedisCache](./Set-AzRedisCache.md)