---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: e550341d0bd5a5d2f4e26e4ac736fab9831b67c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563004"
---
# New-AzureRmAutoscaleNotification

## КРАТКИй обзор
Создает уведомление об автомасштабировании электронной почты.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Максимальное

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzureRmAutoscaleNotification** создает уведомление по электронной почте для автомасштабирования.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Создание уведомления об автомасштабировании электронной почты
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

Эта команда создает уведомление по электронной почте Autosacale для двух указанных адресов.

### Пример 2: Создание уведомления об автомасштабировании электронной почты для администратора подписки
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

Эта команда создает уведомление по электронной почте Autosacale для администратора подписки.

## ПАРАМЕТРЫ

### -CustomEmail
Указывает список адресов электронной почты, разделенных запятыми.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure

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

### -SendEmailToSubscriptionAdministrator
Это означает, что эта операция отправляет администратору подписки уведомление по электронной почте.

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

### -SendEmailToSubscriptionCoAdministrator
Указывает на то, что эта операция отправляет уведомление по электронной почте для соадминистраторов подписки.

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

### -Перехватчик
Задает разделенный запятыми список веб-перехватчиков автомасштабирования.

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Microsoft. Azure. Management. Monitor. Management. Models. WebhookNotification []

### System. String []

### System. Management. Automation. SwitchParameter

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Management. Monitor. Management. Models. AutoscaleNotification

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[New-AzureRmAutoscaleWebhook](./New-AzureRmAutoscaleWebhook.md)


