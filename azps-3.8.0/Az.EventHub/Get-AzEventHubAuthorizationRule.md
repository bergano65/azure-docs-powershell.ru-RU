---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7fa3b4780e4c25dd716b851fd80c698b8d98d0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066294"
---
# Get-AzEventHubAuthorizationRule

## КРАТКИй обзор
Получает сведения о правиле авторизации или получает список правил авторизации.

## Максимальное

### NamespaceAuthorizationRuleSet (по умолчанию)
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventhubAuthorizationRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasAuthoRuleSet
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет Get-AzEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для определенного концентратора событий.
Если указано имя правила авторизации, возвращается информация об этом отдельном правиле авторизации.
Если имя правила авторизации не задано, возвращается список всех правил авторизации для указанного концентратора событий.
Если задано имя псевдонима (аварийное восстановление), возвращается информация о правиле авторизации пространства имен для указанного псевдонима.

## ИЛЛЮСТРИРУЮТ

### Пример 1,0-AuthorizationRule для пространства имен
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .

### Пример 1,1-AuthorizationRules для пространства имен
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Получает список всех правил авторизации в пространстве имен \` MyNamespaceName \` .

### Пример 2,0-AuthorizationRule для EventHub
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

Получает правило авторизации \` MyAuthRuleName \` в MyEventHubName концентратора событий \` \` , область которого ограничена пространством имен \` MyNamespaceName \` .

### Пример 2,1-AuthorizationRules для EventHub
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Получает правила авторизации списка в центре событий \` MyEventHubName \` , областью действия которых является пространство имен \` MyNamespaceName \` .

### Пример 3,0-AuthorizationRule для псевдонима (конфигурация с геовосстановлением)
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

Возвращает правило авторизации \` , MyAuthRuleName \` в пространстве имен \` MyNamespaceName \` .

### Пример 3,1-AuthorizationRules для псевдонима (конфигурация с геовосстановлением)
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

Получает список всех MyAuthRuleName правил авторизации \` \` в пространстве имен \` MyNamespaceName \` .

## ПАРАМЕТРЫ

### -AliasName
Имя псевдонима

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Eventhub
Имя Eventhub

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
Имя AuthorizationRule

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Имя пространства имен

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
