---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 9a17dfd649f35da3fa071eb7c6d2752d3a923398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729880"
---
# Set-AzNotificationHubsNamespace

## КРАТКИй обзор
Задает значения свойств для пространства имен центра уведомлений.

## Максимальное

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Set-AzNotificationHubsNamespace** задает значения свойств существующего пространства имен концентратора уведомлений.
Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.
Необходимо иметь по крайней мере одно пространство имен концентратора уведомлений.
Кроме того, все концентраторы уведомлений должны иметь назначенное пространство имен.
Этот командлет используется преимущественно для включения и отключения пространства имен.
Если пространство имен отключено, пользователи не могут подключаться к каким-либо концентраторам уведомлений в пространстве имен, а также не могут использовать эти концентраторы для отправки push-уведомлений.
Чтобы повторно включить отключенное пространство имен, используйте этот командлет, чтобы задать для свойства **State** пространства имен значение "активно".
Вы также можете использовать этот командлет, чтобы пометить пространство имен как критическое.
Это предотвратит удаление пространства имен.
Чтобы удалить критическое пространство имен, необходимо сначала удалить критический тег.

## ИЛЛЮСТРИРУЮТ

### Пример 1: Отключение пространства имен
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Эта команда отключает пространство имен с именем ContosoPartners, находящееся в центре обработки данных "Западная часть США" и назначенное группе ресурсов ContosoNotificationsGroup.

### Пример 2: включение пространства имен
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Эта команда включает пространство имен с именем ContosoPartners, которое находится в центре обработки данных "Западная часть США" и назначено группе ресурсов ContosoNotificationsGroup.

## ПАРАМЕТРЫ

### -Критический уровень
Указывает, является ли пространство имен критическим для пространства имен.
Не удается удалить критические пространства имен.
Чтобы удалить критическое пространство имен, необходимо установить для этого свойства значение false, чтобы помечать пространство имен как некритическое.

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
Не запрашивать подтверждение.

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
Указывает отображаемое имя центра обработки данных, на котором размещается пространство имен.
Несмотря на то, что вы можете установить для этого параметра любое допустимое расположение Azure, для оптимальной производительности следует использовать центр обработки данных, расположенный рядом с большинством пользователей.
Чтобы получить актуальный список местоположений Azure, выполните следующую команду: `Get-AzLocation | Select-Object DisplayName`

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
Задает пространство имен, которое изменяет этот командлет.
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

### -ResourceGroup
Указывает группу ресурсов, которой назначено пространство имен.
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
Указывает текущее состояние пространства имен.
Допустимые значения этого параметра: активны и отключены.

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

### -Тег
Указывает пары "имя-значение", которые можно использовать для классификации и упорядочения элементов Azure.
Теги похожи на ключевые слова и работают в рамках развертывания.
Например, если вы ищете все элементы в отделе тегов: поиск вернет все элементы Azure с таким тегом, независимо от того, как тип элемента, расположение или группа ресурсов.
Отдельный тег состоит из двух частей: *имени* и (необязательно) *значения*.
Например, в отделе: имя тега — "Отдел", а значение тега —.
Чтобы добавить тег, используйте синтаксис хэш-таблицы, аналогичный приведенному ниже, который создает тег CalendarYear: 2016:-Tags @ {Name = "CalendarYear"; Value = "2016"} чтобы добавить несколько тегов в одной команде, разделите отдельные Теги с помощью запятых:-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "FiscalYear"; Value = "2017"}

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
Запрашивает подтверждение перед запуском командлета.

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
Показывает, что произойдет при запуске командлета. Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### System. String

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceState

### System. Boolean

### System. Collections. Hashtable

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


