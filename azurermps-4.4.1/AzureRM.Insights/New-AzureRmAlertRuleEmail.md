---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566712"
---
# New-AzureRmAlertRuleEmail

## КРАТКИй обзор
Создание действия электронной почты для правила оповещения.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmAlertRuleEmail** создает действие электронной почты для правила оповещения.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание действия по электронной почте правила оповещения для владельцев служб
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

Эта команда создает действие по электронной почте правила оповещения, которое отправляется своим владельцам услуг при срабатывании правила оповещения.

### Пример 2: Создание действия по электронной почте для правила оповещения для владельцев, не связанных с обслуживанием
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

Эта команда создает действие по электронной почте правила оповещения для указанных адресов электронной почты, но не для владельцев служб.

### Пример 3: Создание действия по электронной почте правила оповещения для владельцев услуг и не владельцев служб
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

Эта команда создает действие по электронной почте правила оповещения для указанного адреса и для владельцев служб.

## ПАРАМЕТРЫ

### -CustomEmails
Задает список адресов электронной почты, разделенных запятыми.

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

### -SendToServiceOwners
Указывает, что эта операция отправляет владельцам службы сообщение электронной почты при срабатывании правила.

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

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. Monitor. Management. Models. RuleEmailAction

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Add-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[New-AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


