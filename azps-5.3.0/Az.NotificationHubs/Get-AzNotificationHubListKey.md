---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 062d16155d4e1644e09f914a1114741e7bc5365f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517838"
---
# Get-AzNotificationHubListKey

## SYNOPSIS
Возвращает основные и дополнительные строки подключения, связанные с правилом авторизации концентратора уведомлений.

## СИНТАКСИС

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Чтобы **получить основное** и дополнительное строки подключения для правила авторизации SAS, можно получить главное и дополнительное строки подключения для правила авторизации в Центре уведомлений Shared Access Signature (SAS).
Правила авторизации управляют правами пользователей на центр.
Каждое правило содержит основную и вторичную строку подключения.
Эти строки подключения ( URIS) выполняют указанные ниже точки.
- Наказать пользователей на ресурс.
- Включайте маркер, содержащий параметры запроса.
Один из этих параметров ( подпись) используется для проверки подлинности пользователя и обеспечивает указанный уровень доступа.

## ПРИМЕРЫ

### Пример 1. Получите основные и дополнительные строки подключения для правила авторизации
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Эта команда получает основные и дополнительные строки подключения для правила авторизации ListenRule — правила, назначенного концентратору уведомлений ContosoInternalHub.
Команда должна включать пространство имен концентратора и группу ресурсов.

## PARAMETERS

### -AuthorizationRule
Указывает имя правила проверки подлинности SAS.
Эти правила определяют тип доступа пользователей к центру уведомлений.

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
Определяет пространство имен, которому назначен концентратор уведомлений.
Пространства имен предоставляют возможность группировать и классифицировать концентраторы уведомлений.

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
Указывает центр уведомлений, для который этот cmdlet назначает правило авторизации.
Концентраторы уведомлений используются для отправки push-уведомлений нескольким клиентам независимо от платформы, используемой этими клиентами.

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
Группа ресурсов, которой назначен концентратор уведомлений.
Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.

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
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## OUTPUTS

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)


