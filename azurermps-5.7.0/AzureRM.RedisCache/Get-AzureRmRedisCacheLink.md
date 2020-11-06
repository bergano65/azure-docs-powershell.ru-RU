---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheLink.md
ms.openlocfilehash: dff5f565e27f89360465ede3eb8fbe2c3d5620a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561587"
---
# Get-AzureRmRedisCacheLink

## КРАТКИй обзор
Получение ссылки на георепликацию для Redis кэша.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### AllLinksForCache (по умолчанию)
```
Get-AzureRmRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForPrimaryCache
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SingleLink
```
Get-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AllLinksForSecondaryCache
```
Get-AzureRmRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Существует четыре способа получения сведений о ссылке георепликации. Укажите имя параметра или PrimaryServerName или SecondaryServerName. Имя, после чего будет возвращена ссылка на то, где находится кэш. Если задано только PrimaryServerName, будут возвращены все ссылки, в которых хранится кэш PRIMARY. Если задано только SecondaryServerName, будут возвращены все ссылки, в которых должен быть указан дополнительный кэш. Если заданы оба PrimaryServerName и SecondaryServerName, будет возвращена определенная ссылка на соответствующую роль. 

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение параметров с помощью Set AllLinksForCache
```
PS C:\>Get-AzureRmRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Эта команда получает все ссылки георепликации для кэша Redis с именем mycache1.

### Пример 2: получение параметров с помощью Set AllLinksForPrimaryCache
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Эта команда получает ссылки на георепликацию, где кэш Redis с именем mycache1 является основным.

### Пример 3: получение параметров с помощью Set AllLinksForSecondaryCache
```
PS C:\>Get-AzureRmRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Эта команда получает ссылки на георепликацию, где кэш Redis с именем mycache2 является дополнительным.

### Пример 4: получение параметров с помощью Set SingleLink
```
PS C:\>Get-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Эта команда получает одну ссылку на георепликацию, в которой кэш Redis с именем mycache1 является основным, а Redis кэш с именем mycache2 — дополнительным.

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
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrimaryServerName
Имя основного кэша Redis в ссылке.

```yaml
Type: String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryServerName
Имя вспомогательного кэша Redis в ссылке.

```yaml
Type: String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
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

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. RedisCache. Models. PSRedisLinkedServer, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = Neutral, PublicKeyToken = NULL]]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmRedisCacheLink](./New-AzureRmRedisCacheLink.md)

[Remove-AzureRmRedisCacheLink](./Remove-AzureRmRedisCacheLink.md)

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[New-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)
