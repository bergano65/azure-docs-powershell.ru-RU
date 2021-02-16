---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225601"
---
# Get-AzNotificationHubAuthorizationRule

## SYNOPSIS
Получает сведения о правилах авторизации, связанных с центром уведомлений.

## СИНТАКСИС

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## ОПИСАНИЕ
С **помощью cmdlet Get-AzNotificationHubAuthorizationRule** можно получить сведения о правилах авторизации saS, связанных с центром уведомлений.
Он возвращает сведения обо всех правилах, связанных с центром, или, в том числе с параметром *AuthorizationRule,* получает сведения об определенном правиле.
Правила авторизации управляют доступом к концентраторам уведомлений.
Правило авторизации создает ссылки в качестве URI на основе различных уровней разрешений.
Клиенты направляются на один из этих URL-адресов с учетом соответствующего уровня разрешений.
Например, клиент с разрешением "Прослушивание" будет направлен в URI для этого разрешения.
С **помощью cmdlet Get-AzNotificationHubAuthorizationRule** можно получить сведения только о правилах авторизации, связанных с центром уведомлений.
Чтобы получить сведения о самом центре, используйте Get-AzNotificationHub.

## ПРИМЕРЫ

### Пример 1. Получите сведения для всех правил авторизации, которые назначены центру уведомлений
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Эта команда получает сведения для всех правил авторизации, которые назначены центру уведомлений ContosoInternalHub в области имен ContosoNamespace.
Необходимо указать пространство имен, в котором находится центр, а также группу ресурсов, которой он назначен.

### Пример 2. Получите сведения о правилах авторизации, которые назначены центру уведомлений
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Эта команда получает сведения для всех правил авторизации, которые назначены центру уведомлений ContosoInternalHub в области имен ContosoNamespace.
Команда использует параметр *AuthorizationRule,* чтобы ограничить возвращенные данные одним правилом авторизации с именем ListenRule.

## PARAMETERS

### -AuthorizationRule
Указывает имя правила проверки подлинности SAS.
Эти правила определяют тип доступа пользователей к центру уведомлений.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.

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
Указывает центр уведомлений, который этим cmdlet назначает правила авторизации.
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
Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, упрощая управление запасами и администрирование Azure.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubAuthorizationRule](./New-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


