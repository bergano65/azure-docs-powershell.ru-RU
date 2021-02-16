---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225580"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Создание пространства имен концентратора уведомлений.

## СИНТАКСИС

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## ОПИСАНИЕ
Для создания пространства имен концентратора уведомлений создается **cmdlet New-AzNotificationHubsNamespace.**
Пространства имен — это логические контейнеры, которые помогают организовать концентраторы уведомлений и управлять ими.
Необходимо иметь хотя бы одно пространство имен концентратора уведомлений.
В одном пространстве имен может быть несколько концентраторов.
Вы можете использовать несколько пространства имен, чтобы упорядочеть концентраторы или предоставить определенным людям разрешение на управление выбранным подмножеством ваших концентраторов.
Чтобы создать пространство имен, укажите уникальное имя для пространства имен. указать центр обработки данных, в котором будет расположено пространство имен; и укажите группу ресурсов, которая будет назначена области имен.
После создания пространства имен можно использовать New-AzNotificationHubsNamespaceAuthorizationRules для назначения в него правил авторизации.
Правила авторизации используются для управления разрешениями на доступ к области имен.

## ПРИМЕРЫ

### Пример 1. Создание концентратора уведомлений
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Эта команда создает концентратор уведомлений ContosoPartners.
Пространство имен будет расположено в центре обработки данных Западной части США и назначено группе ресурсов ContosoNotificationsGroup.

### Пример 2. Создание концентратора уведомлений с тегами
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Эта команда создает концентратор уведомлений ContosoPartners.
Пространство имен будет расположено в центре обработки данных Западной части США и назначено группе ресурсов ContosoNotificationsGroup.
Кроме того, эта команда создает тег с именем Audience и значением PartnerOrganizations и которая назначена области имен.
Это гарантирует, что пространство имен будет отображаться при фильтрации элементов, для которых тегу аудитории назначено имя PartnerOrganizations.

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

### -Location
Указывает отображаемую имя центра обработки данных, в который будет вмечено пространство имен.
Хотя для этого параметра можно установить любое допустимый расположение, для оптимальной работы может потребоваться использовать центр обработки данных, расположенный рядом с большинством пользователей.

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

### -Namespace
Указывает имя нового пространства имен.
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
Группа ресурсов, которой будет назначено пространство имен.
Группы ресурсов упорядочиют такие элементы, как пространства имен, концентраторы уведомлений и правила авторизации, чтобы упрость управление запасами и администрирование.

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

### -SkuTier
Уровень SKU пространства имен

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Определяет пары "имя-значение", которые можно использовать для классификации и у организовывать элементы Azure.
Теги работают так же, как ключевые слова, и работают в развертывании.
Например, при поиске всех элементов с тегом Department:IT поиск возвратит все элементы Azure, которые имеют этот тег, независимо от типа элемента, расположения или группы ресурсов.
Отдельный тег состоит из двух частей: *"Имя"* и (при желании) *"Значение".*
Например, в отделе Department:IT имя тега — Department, а значение тега — IT.
Чтобы добавить тег, используйте синтаксис таблицы с шестн. При этом создается тег CalendarYear:2016:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Перед запуском cmdlet вам будет предложено подтвердить его.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Показывает, что произойдет при запуске cmdlet. Этот cmdlet не будет выполниться.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


