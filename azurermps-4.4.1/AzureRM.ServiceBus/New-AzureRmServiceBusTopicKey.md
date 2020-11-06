---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562167"
---
# New-AzureRmServiceBusTopicKey

## КРАТКИй обзор
Повторно создает первичные или дополнительные строки подключения для раздела служебной шины.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmServiceBusTopicKey** создает новую первичную или вспомогательную строку подключения для указанной темы служебной шины и правила авторизации.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

Повторно создает основную строку подключения для пространства имен.

### Пример 2
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

Повторно создает вспомогательную строку подключения для пространства имен.

## ПАРАМЕТРЫ

### -RegenerateKeys
Указывает, следует ли повторно создавать первичные или вторичные ключи.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -Name (имя)
Имя правила авторизации.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Имя пространства имен.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Темы
Название раздела.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### -ResourceGroup
 System. String
 

### -+ +
 System. String
 

### -AuthorizationRuleName
 System. String
 

### -TopicName
 System. String
 

### -RegenerateKeys
 System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. ServiceBus. Models. ListKeysAttributes
PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-Topi c_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.NET/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-value}; EntityPath = SB-Topi c_exampl1 PrimaryKey: {value PrimaryKey} SecondaryKey: {SecondaryKey значение} KeyName: SBTopicAuthoRule1

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

