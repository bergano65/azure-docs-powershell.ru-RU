---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563535"
---
# Get-AzureRmEventHub

## КРАТКИй обзор
Получение сведений об одном концентраторе событий или получение списка концентраторов событий.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmEventHub возвращает либо сведения о концентраторе событий, либо список всех концентраторов событий в текущем пространстве имен.
Если указано имя концентратора событий, возвращаются сведения об одном концентраторе событий.
Если имя концентратора событий не указано, возвращается список всех концентраторов событий в указанном пространстве имен.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Возвращает сведения о концентраторе событий \` MyEventHubName \` .

### Пример 2
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

Возвращает список концентраторов событий в MyNamespaceName пространства имен \` \` .

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
Имя EventHub

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Имя пространства имен

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
Parameter Sets: (All)
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

### System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.5.0.0, культура = нейтраль, PublicKeyToken = NULL]]


## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
