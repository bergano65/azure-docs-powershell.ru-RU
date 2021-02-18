---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240504"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
Получает сведения о пространстве имен концентратора уведомлений.

## СИНТАКСИС

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## ОПИСАНИЕ
Чтобы получить сведения о пространствах имен концентратора уведомлений, можно получить сведения о **cmdlet Get-AzNotificationHubsNamespace.**
Этот cmdlet обеспечивает получение сведений обо всех пространствах имен, а также об пространствах имен, которые назначены указанной группе ресурсов. или для получения сведений об определенном пространстве имен.
Пространства имен — это логические контейнеры, которые помогают организовать концентраторы уведомлений и управлять ими.
Необходимо иметь хотя бы одно пространство имен концентратора уведомлений: все концентраторы уведомлений должны быть назначены для пространства имен.
В одном пространстве имен может быть несколько концентраторов, что означает, что в вашей организации может потребоваться только одно пространство имен.
Однако вы также можете использовать несколько пространства имен для более эффективного у упорядочества концентраторов или для того, чтобы предоставить определенным людям разрешение на управление выбранным подмножеством концентраторов.
Для получения основных сведений о самом пространстве имен возвращается **cmdlet Get-AzNotificationHubsNamespace.**
Чтобы получить сведения о правилах авторизации, связанных с пространством имен, используйте Get-AzNotificationHubsNamespaceAuthorizationRules.

## ПРИМЕРЫ

### Пример 1. Получить сведения для всех пространства имен концентратора уведомлений
```
PS C:\>Get-AzNotificationHubsNamespace
```

Эта команда возвращает сведения для всех пространства имен концентратора уведомлений.

### Пример 2. Получите сведения для одного пространства имен концентратора уведомлений
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Эта команда получает сведения для единого пространства имен концентратора уведомлений: ContosoNamespace.

### Пример 3. Сведения для всех концентраторов уведомлений, которые назначены определенному пространству имен
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Эта команда получает сведения для всех пространства имен концентратора уведомлений, которые назначены группе ресурсов ContosoNotificationsGroup.

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

### -Namespace
Указывает уникальное имя пространства имен.
Пространства имен предоставляют возможность группировать концентраторы уведомлений и классифицировать их.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Группа ресурсов, которой назначено пространство имен.
Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


