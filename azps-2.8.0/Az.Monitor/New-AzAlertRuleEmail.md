---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: e7ba5bc42e08ce73fcfac5fcbb7ea614a43f2b3e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397889"
---
# New-AzAlertRuleEmail

## SYNOPSIS
Создает действие по электронной почте для правила оповещения.

## СИНТАКСИС

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Для правила оповещения создается действие **"New-AzAlertRuleEmail".**

## ПРИМЕРЫ

### Пример 1. Создание действия правила оповещения для владельцев служб
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Эта команда создает действие правила оповещения, которое отправляется владельцам служб при его отправке.

### Пример 2. Создание действия правила оповещения для владельцев, не внося в службу
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

Эта команда создает действие правила оповещения для указанных адресов электронной почты, но не для владельцев служб.

### Пример 3. Создание действия правила оповещения для владельцев служб и других владельцев
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

Эта команда создает действие правила оповещения для указанного адреса и для его владельцев служб.

## PARAMETERS

### -CustomEmail
Список адресов электронной почты, разделенных запятой.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -SendToServiceOwner
Указывает на то, что при отправке правила владельцам службы отправляется сообщение электронной почты.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String[]

### System.Management.Automation.SwitchParameter

## OUTPUTS

### Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ


[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


