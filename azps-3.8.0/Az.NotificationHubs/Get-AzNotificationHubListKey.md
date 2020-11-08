---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: b8fdacf86de0e85c6f0ce241e743fc73066beb71
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065797"
---
# Get-AzNotificationHubListKey

## КРАТКИй обзор
Получает первичные и вторичные строки подключения, связанные с правилом авторизации концентратора уведомлений.

## Максимальное

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzNotificationHubListKey** возвращает первичные и дополнительные строки подключения для правила авторизации на основе центра уведомлений (SA).
Правила авторизации управляют правами пользователей на разветвитель.
Каждое правило включает в себя первичную и вспомогательную строку подключения.
Эти строки подключения (URI) выполняют указанные ниже действия.
- Наведите пользователей на ресурс.
- Добавьте токен, содержащий параметры запроса.
Один из этих параметров — подпись используется для проверки подлинности пользователя и предоставления указанного уровня доступа.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение первичных и дополнительных строк подключения для правила авторизации
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Эта команда получает первичные и дополнительные строки подключения для правила авторизации ListenRule, правило, назначенное для концентратора уведомлений ContosoInternalHub.
Команда должна включать пространство имен HUB и группу ресурсов.

## ПАРАМЕТРЫ

### -AuthorizationRule
Указывает имя правила проверки подлинности для подписи общего доступа (SAS).
Эти правила определяют тип доступа пользователей к концентратору уведомлений.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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

### -Namespace
Задает пространство имен, которому назначен Центр уведомлений.
Пространства имен обеспечивают способ группировки и классификации концентраторов уведомлений.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
Указывает центр уведомлений, которому назначается правило авторизации с помощью этого командлета.
Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам вне зависимости от платформы, используемой этими клиентами.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Указывает группу ресурсов, которой назначен Центр уведомлений.
Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, в целях простого управления запасами и администрирования Azure.

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

### Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzNotificationHubAuthorizationRules](./Get-AzNotificationHubAuthorizationRules.md)


