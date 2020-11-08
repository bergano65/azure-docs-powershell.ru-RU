---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076549"
---
# Get-AzureStorSimpleResourceContext

## КРАТКИй обзор
Возвращает текущий контекст ресурса.

## Максимальное

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureStorSimpleResourceContext** получает текущий контекст ресурсов.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение текущего контекста
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

Первая команда задает текущий контекст как ресурс с именем Contoso63-Tsqa с помощью командлета **SELECT-AzureStorSimpleResource** .

Вторая команда возвращает текущий контекст ресурса.

### Пример 2. попытка получить текущий контекст
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

Эта команда возвращает текущий контекст.
В этом примере контекст не установлен.
Команда возвращает сообщение с описанием проблемы.

## ПАРАМЕТРЫ

### -Profile
Указывает профиль Azure.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

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

## НАПРЯЖЕНИЕ

### StorSimpleResourceContext
Этот командлет возвращает объект **разделе ResourceContext** .

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[SELECT-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


