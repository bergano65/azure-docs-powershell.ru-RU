---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: a9675f2473488d1415a83ae0454a3841cd10d589
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729899"
---
# New-AzNotificationHubsNamespace

## КРАТКИй обзор
Создает пространство имен концентратора уведомлений.

## Максимальное

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **New-AzNotificationHubsNamespace** создает пространство имен концентратора уведомлений.
Пространства имен — это логические контейнеры, помогающие упорядочивать концентраторы уведомлений и управлять ими.
Необходимо иметь по крайней мере одно пространство имен концентратора уведомлений.
Одно пространство имен может быть размещено на нескольких ступицах.
Вы можете использовать несколько пространств имен для Организации концентраторов или предоставить определенным пользователям разрешение на управление выбранной подмножеством концентраторов.
Чтобы создать пространство имен, убедитесь, что вы указали уникальное имя для пространства имен. Укажите центр обработки данных, в котором будет находиться пространство имен; Укажите группу ресурсов, которой будет назначено пространство имен.
После создания пространства имен можно использовать командлет New-AzNotificationHubsNamespaceAuthorizationRules для назначения правил авторизации этому пространству имен.
Правила авторизации используются для управления разрешениями пространства имен.

## ИЛЛЮСТРИРУЮТ

### Пример 1: создание концентратора уведомлений
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Эта команда создает концентратор уведомлений с именем ContosoPartners.
Пространство имен будет находиться в центре обработки данных "Западная часть США" и назначено группе ресурсов ContosoNotificationsGroup.

### Пример 2: создание концентратора уведомлений с помощью тегов
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Эта команда создает концентратор уведомлений с именем ContosoPartners.
Пространство имен будет находиться в центре обработки данных "Западная часть США" и назначено группе ресурсов ContosoNotificationsGroup.
Кроме того, эта команда создает тег с именем аудитории и значением PartnerOrganizations и назначается пространству имен.
Это гарантирует, что во время фильтрации для элементов, в которых тег аудитории имеет значение PartnerOrganizations, будет отображаться пространство имен.

## ПАРАМЕТРЫ

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
Указывает отображаемое имя центра обработки данных, на котором будет размещено пространство имен.
Несмотря на то, что вы можете установить для этого параметра любое допустимое расположение, для оптимальной производительности может потребоваться центр обработки данных, находящийся рядом с большинством пользователей.

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
Указывает группу ресурсов, которой будет назначено пространство имен.
Группы ресурсов организуют элементы, такие как пространства имен, концентраторы уведомлений и правила авторизации, таким образом, чтобы упростить управление запасами и администрирование.

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

### -Тег
Указывает пары "имя-значение", которые можно использовать для классификации и упорядочения элементов Azure.
Теги похожи на ключевые слова и работают в рамках развертывания.
Например, если вы ищете все элементы в отделе тегов: поиск вернет все элементы Azure с таким тегом, независимо от того, как тип элемента, расположение или группа ресурсов.
Отдельный тег состоит из двух частей: *имени* и, при необходимости, *значения*.
Например, в отделе: имя тега — "Отдел", а значение тега —.
Чтобы добавить тег, используйте синтаксис хэш-таблицы, аналогичный приведенному ниже, который создает тег CalendarYear: 2016:

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

### System. Collections. Hashtable

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. NotificationHubs. Models. NamespaceAttributes

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


