---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395279"
---
# Get-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Получает сведения о правилах авторизации, связанных с пространством имен концентратора уведомлений.

## СИНТАКСИС

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Cmdlet **Get-AzNotificationHubsNamespaceAuthorizationRule** возвращает сведения о правилах авторизации подписи общего доступа (SAS), связанных с пространством имен концентратора уведомлений.
Вы можете вернуть сведения обо всех правилах, связанных с пространством имен.
Кроме того, с помощью параметра *AuthorizationRule* можно вернуть сведения для определенного правила.
Правила авторизации управляют доступом к пространствам имен.
Это делается путем создания ссылок ( URIS) на основе различных уровней разрешений.
Для платформы можно использовать один из следующих уровней: 
- Прослушивание
- Отправить
- Управление клиентами направляется на один из этих ЮРИСов с учетом соответствующего уровня разрешений.
Например, клиент с разрешением на прослушивание будет направлен в URI для этого разрешения.
Этот cmdlet получает только правила авторизации, связанные с пространством имен.
Чтобы получить сведения о самом пространстве имен, используйте Get-AzNotificationHubsNamespace.

## ПРИМЕРЫ

### Пример 1. Просмотр сведений обо всех правилах авторизации, которые назначены пространствам имен
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Эта команда получает сведения обо всех правилах авторизации, которые назначены для пространства имен ContosoNamespace и группы ресурсов ContosoNotificationsGroup.

### Пример 2. Просмотр сведений о правиле авторизации
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Эта команда получает сведения об одном правиле авторизации пространства имен с именем ListenRule.
При получения сведений о конкретном правиле авторизации необходимо включить пространство имен и группу ресурсов.

## PARAMETERS

### -AuthorizationRule
Указывает имя правила проверки подлинности SAS.
Эти правила определяют тип доступа пользователей к области имен.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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
Определяет пространство имен, которому назначены правила авторизации.
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

### -ResourceGroup
Группа ресурсов, которой назначены правила авторизации.
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

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


