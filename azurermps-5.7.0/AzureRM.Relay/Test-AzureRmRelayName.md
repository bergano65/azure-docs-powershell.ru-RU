---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566139"
---
# Test-AzureRmRelayName

## КРАТКИй обзор
Проверяет доступность указанного имени пространства имен.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Test-AzureRmRelayName** проверяет доступность имени пространства имен

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### Пример 2
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### Пример 3
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

Возвращает состояние доступности имени пространства имен.

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

### -Namespace
Имя пространства имен ретрансляции.

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

### [Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, культура = Neutral, PublicKeyToken = NULL]

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

