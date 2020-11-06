---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: 5f1e8037e4a9faef508c2ffd62ff00aca4387cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562228"
---
# Get-AzureRmRelayNamespace

## КРАТКИй обзор
Возвращает описание указанного пространства имен ретрансляции в группе ресурсов.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzureRmRelayNamespace** получает описание указанного пространства имен ретрансляции в группе ресурсов.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

Возвращает описание указанного пространства имен ретрансляции.

## ПАРАМЕТРЫ

### -Name (имя)
Имя пространства имен ретрансляции.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
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

### -ResourceGroupName
System. String

### -Name (имя)
 System. String

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Model. RelayNamespaceAttributes, Microsoft. Azure. Commands. ретрансляцией, Version = 0.1.0.0, культура = нейтральная, PublicKeyToken = NULL]]
ProvisioningState: CreatedAt 4/12/2017 12:38:47: UpdatedAt: 4/12/2017 12:39:10 AM ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId: 854d368f-1828-428f-8f3c-f2affa9b2f7d: testnamespace-Relay1 Location: Западная часть US Tags: {[TAG1, Tag1Value]} идентификатор:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-servicebus-WestUS/providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1 имя: TestNameSpace-Relay1 тип: Microsoft. Relay/Namespaces

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

