---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734225"
---
# Test-AzureRmServiceBusName

## КРАТКИй обзор
Проверяет доступность указанного имени пространства имен.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## NОПИСАНИЕ
Командлет **Test-AzureRmServiceBusName** проверяет доступность имени пространства имен

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### Пример 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### Пример 3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

Возвращает состояние доступности имени пространства имен.

## ПАРАМЕТРЫ

### -Namespace
Имя пространства имен ServiceBus.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### -Namespace
 System. String

## НАПРЯЖЕНИЕ

### [Microsoft. Azure. Commands. ServiceBus. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, культура = Neutral, PublicKeyToken = NULL]

### Пример 1
Сообщение о причине NameAvailable
------------- ------ -------
         True   None

### Пример 2
Сообщение о причине NameAvailable
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### Пример 3
Сообщение о причине NameAvailable
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
