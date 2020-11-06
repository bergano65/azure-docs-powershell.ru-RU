---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569500"
---
# Get-AzureRmEventHubAuthorizationRule

## КРАТКИй обзор
Получает сведения о правиле авторизации или получает список правил авторизации.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### NamespaceAuthorizationRuleSet (по умолчанию)
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### EventhubAuthorizationRuleSet
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## NОПИСАНИЕ
Командлет Get-AzureRmEventHubAuthorizationRule получает либо сведения о правиле авторизации, либо список всех правил авторизации для определенного концентратора событий.
Если указано имя правила авторизации, возвращается информация об этом отдельном правиле авторизации.
Если имя правила авторизации не задано, возвращается список всех правил авторизации для указанного концентратора событий.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

Получает правило авторизации \` MyAuthRuleName \` в MyEventHubName концентратора событий \` \` , область которого ограничена пространством имен \` MyNamespaceName \` .

### Пример 2
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

Получает список всех правил авторизации в концентраторе событий \` MyEventHubName \` , область которого ограничена пространством имен \` MyNamespaceName \` .

## ПАРАМЕТРЫ

### -ResourceGroupName
Имя группы ресурсов.

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

### -Eventhub
Имя Eventhub.

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (имя)
AuthorizationRule имя.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Имя пространства имен.

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## ВХОДНЫЕ данные

### System. String

## НАПРЯЖЕНИЕ

### System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. eventhub, версия = 0.0.1.0, культура = нейтраль, PublicKeyToken = NULL]]

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

