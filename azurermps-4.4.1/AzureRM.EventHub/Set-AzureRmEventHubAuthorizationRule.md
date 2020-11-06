---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566724"
---
# Set-AzureRmEventHubAuthorizationRule

## КРАТКИй обзор
Обновляет указанное правило авторизации на концентраторе событий.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

### NamespaceAuthorizationRuleSet (по умолчанию)
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### EventhubAuthorizationRuleSet
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### AuthoRuleInputObjectSet
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### AuthoRulePropertiesSet
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## NОПИСАНИЕ
Командлет Set-AzureRmEventHubAuthorizationRule обновляет указанное правило авторизации на данном концентраторе событий.

## ИЛЛЮСТРИРУЮТ

### Пример 1
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

Обновляет MyAuthRuleName правила авторизации \` \` , чтобы предоставить доступ к управлению правами для центра событий \` MyEventHubName \` , областью которого является пространство имен \` MyNamespaceName \` .

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

### -Права
Обязательно, если не указана "AuthruleObj".
Администратора Например, @ ("прослушать", "Отправить", "Управление")

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Запрашивает подтверждение перед запуском командлета.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventHub
Имя EventHub.

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

### -InputObject
{{Fill InputObject описание}}

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (имя)
AuthorizationRule имя.

```yaml
Type: String
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

### Microsoft. Azure. Commands. EventHub. Models. SharedAccessAuthorizationRuleAttributes

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

