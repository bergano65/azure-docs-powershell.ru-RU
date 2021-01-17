---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395199"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
Задает значения свойств для пространства имен концентратора уведомлений.

## СИНТАКСИС

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## ОПИСАНИЕ
Для свойства существующего пространства имен концентратора уведомлений задаются значения свойств **set-AzNotificationHubsNamespace.**
Пространства имен — это логические контейнеры, которые помогают организовать концентраторы уведомлений и управлять ими.
Необходимо иметь по крайней мере одно пространство имен концентратора уведомлений.
Кроме того, у всех концентраторов уведомлений должно быть назначено пространство имен.
Этот cmdlet в основном используется для того, чтобы включить и отключить пространство имен.
Если пространство имен отключено, пользователи не могут подключаться к концентраторам уведомлений в этом пространстве и администраторы не могут использовать их для отправки push-уведомлений.
Чтобы снова включить отключенное пространство имен, с помощью этого cmdlet можно установить для свойства **State** пространства имен состояние Active (Состояние) области имен.
С помощью этого командлета можно также пометить пространство имен как важное.
Это предотвращает удаление пространства имен.
Чтобы удалить критическое пространство имен, сначала необходимо удалить критический тег.

## ПРИМЕРЫ

### Пример 1. Отключение пространства имен
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Эта команда отключает пространство имен "ContosoPartners", расположенное в центре обработки данных "Запад США", и назначено группе ресурсов ContosoNotificationsGroup.

### Пример 2. Включить пространство имен
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Эта команда включает пространство имен ContosoPartners в центре обработки данных "Запад. США" и назначено группе ресурсов ContosoNotificationsGroup.

## PARAMETERS

### -Критическое
Указывает, является ли пространство имен критическим.
Критически важные области имен удалить нельзя.
Чтобы удалить критическое пространство имен, необходимо указать для этого свойства значение False ( False), чтобы пометить его как некритическое.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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

### -Force
Не спрашивайте подтверждения.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Указывает отображаемого имя центра обработки данных, на котором размещено пространство имен.
Хотя для этого параметра можно установить любое допустимый расположение Azure, для оптимальной работы следует использовать центр обработки данных, расположенный рядом с большинством пользователей.
Чтобы получить список местоположений Azure, запустите следующую команду: `Get-AzLocation | Select-Object DisplayName`

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
Определяет пространство имен, которое изменяет этот cmdlet.
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

### -ResourceGroup
Группа ресурсов, которой назначено пространство имен.
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

### -State
Определяет текущее состояние пространства имен.
Допустимые значения этого параметра: активные и отключенные.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Определяет пары значений имен, которые можно использовать для классификации и у организовывать элементы Azure.
Теги работают так же, как ключевые слова, и работают в развертывании.
Например, при поиске всех элементов с тегом Department:IT поиск возвратит все элементы Azure, которые имеют этот тег, независимо от типа элемента, расположения или группы ресурсов.
Отдельный тег состоит из двух частей: *имя* и (необязательно) *значение.*
Например, в отделе Department:IT имя тега — "Отдел", а значением тега — ИТ.
Чтобы добавить тег, используйте синтаксис таблицы с шестн. При этом создается тег CalendarYear:2016: -Tags @{Name="CalendarYear"; Value="2016"} Чтобы добавить несколько тегов в одной команде, разделите отдельные теги запятой: -Tag @{Name="CalendarYear"; Value="2016"}, @{Name="FiscalYear"; Value="2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Запрос на подтверждение перед запуском cmdlet.

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

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState

### System.Boolean

### System.Collections.Hashtable

## OUTPUTS

### Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes

## ПРИМЕЧАНИЯ

## СВЯЗАННЫЕ ССЫЛКИ

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


