---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563523"
---
# Test-AzureRmEventHubName

## КРАТКИй обзор
Проверяет доступность указанного имени пространства имен или псевдонима (имя конфигурации DR).

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### NamespaceCheckNameAvailabilitySet (по умолчанию)
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasCheckNameAvailabilitySet
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Test-AzureRmEventhubName** проверяет доступность имени или псевдонима пространства имен (имя конфигурации DR).

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

Возвращает состояние доступности имени пространства имен "MyNameSapceName" как истина.

### Пример 2
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

Возвращает состояние доступности имени пространства имен "MyNameSapceName" как false с указанием причины

### Пример 3
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

Возвращает состояние доступности имени псевдонима "myAliasName" в разделе Namespace "MyNameSapceName" как истина

## ПАРАМЕТРЫ

### -AliasName
Имя конфигурации DR — имя псевдонима

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Имя пространства имен Eventhub

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

### -ResourceGroupName
Имя группы ресурсов

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.
Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String


## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. EventHub. Models. PSCheckNameAvailabilityResultAttributes


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
