---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/test-azurermservicebusname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: a35487b2eb1dae8d8af452fba9a47854ecab6efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561464"
---
# Test-AzureRmServiceBusName

## КРАТКИй обзор
Проверяет доступность указанного имени пространства имен или псевдонима (имя конфигурации DR). 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### AliasCheckNameAvailabilitySet
```
Test-AzureRmServiceBusName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NamespaceCheckNameAvailabilitySet
```
Test-AzureRmServiceBusName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Test-AzureRmServiceBusName** проверяет доступность имени или псевдонима пространства имен (имя конфигурации DR).

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

Возвращает состояние доступности имени пространства имен "MyNameSapceName" как истина.

### Пример 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace MyNameSapceName
```

Возвращает состояние доступности имени пространства имен "MyNameSapceName" как false с указанием причины

### Пример 3
```
PS C:\> Test-AzureRmServiceBusName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```


## ПАРАМЕТРЫ

### -AliasName
Имя конфигурации DR — имя псевдонима

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: Alias

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
Имя пространства имен servicebus

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases: ResourceGroup

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

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. PSCheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.5.0.0, Culture = Neutral, PublicKeyToken = NULL]]


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
