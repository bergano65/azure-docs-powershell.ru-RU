---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 8410ca475ed17376e01a526512d758c4712f2726
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411285"
---
# New-AzAlertRuleWebhook

## SYNOPSIS
Создает правило оповещения webhook.

## СИНТАКСИС

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания правила оповещения webhook будет создаваться **cmdlet New-AzAlertRuleWebhook.**

## ПРИМЕРЫ

### Пример 1. Создание веб-приложения "Правило оповещения"
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

Эта команда создает правило оповещения с указанием только URI службы.

### Пример 2. Создание веб-сайта с одним свойством
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

Эта команда создает веб-сайт правила оповещения для Contoso.com с одним свойством, а затем сохраняет его в $Actual переменной.

## PARAMETERS

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -Свойство
Список свойств в формате @(свойство1 = 'значение1',....).

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceUri
Указывает URI службы.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ


[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleEmail](./New-AzAlertRuleEmail.md)

[New-AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


