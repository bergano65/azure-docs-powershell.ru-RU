---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910513"
---
# Close-AzsAlert

## КРАТКИй обзор
Закрывает заданное оповещение.

## Максимальное

### CloseExpanded (по умолчанию)
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Неожиданно
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### CloseViaIdentity
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CloseViaIdentityExpanded
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## NОПИСАНИЕ
Закрывает заданное оповещение.

## ИЛЛЮСТРИРУЮТ

### Пример 1:
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

Закрыть оповещение по имени.

### Пример 2:
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

Закрывайте оповещение с помощью трубопроводов.

## ПАРАМЕТРЫ

### -Alert (оповещение)
Этот объект представляет собой предупредительный ресурс.
Для конструирования ознакомьтесь с разделом "Заметки" для свойств оповещения и создайте хэш-таблицу.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -AlertId
Возвращает или задает идентификатор оповещения.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -AlertProperty
Свойства оповещения.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ClosedByUserAlias
Псевдоним пользователя, который закрыл оповещение.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ClosedTimestamp
Временная метка, когда оповещение было закрыто.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -CreatedTimestamp
Метка времени создания оповещения.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Описание
Описание оповещения.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -FaultId
Возвращает или задает идентификатор ошибки оповещения.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -FaultTypeId
Возвращает или задает код типа ошибки для оповещения.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -HasValidRemediationAction
Указывает, можно ли исправить это оповещение.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ImpactedResourceDisplayName
Отображаемое имя затронутого элемента.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ImpactedResourceId
Возвращает или задает идентификатор ресурса для затронутого элемента.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -LastUpdatedTimestamp
Метка времени последнего обновления оповещения.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Location
Название региона

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Location1
Регион Azure, в котором находится ресурс

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name (имя)
Имя оповещения.

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Исправление
Возвращает или задает понятные инструкции по исправлению для оповещения.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceGroupName
Имя группы ресурсов.

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceProviderRegistrationId
Возвращает или задает регистрационный идентификатор службы, которой принадлежит оповещение.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceRegistrationId
Возвращает или задает идентификатор регистрации ресурса, связанного с оповещением.
Если оповещение не связано с ресурсом, идентификатор регистрации ресурса равен null.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Серьезность
Уровень опасности оповещения.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -State
Состояние оповещения.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.
Идентификатор подписки образует часть URI для каждого вызова службы.

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -Тег
Теги ресурсов.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Title
Возвращает или задает идентификатор ресурса для затронутого элемента.

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Пользователь
Имя пользователя, используемое для выполнения операции.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Показывает, что произойдет при запуске командлета.
Командлет не выполняется.

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
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## ВХОДНЫЕ данные

### Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IAlert

### Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity

## НАПРЯЖЕНИЕ

### Microsoft. Azure. PowerShell. командлеты. InfrastructureInsightsAdmin. Models. Api20160501. IAlert



## Пуск

Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства. Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.

ПРЕДУПРЕЖДЕНИЕ <IAlert> : этот объект представляет собой предупредительный ресурс.
  - `[Location <String>]`: Область Azure, в которой находится ресурс
  - `[Tag <ITrackedResourceTags>]`: Теги ресурсов.
    - `[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.
  - `[AlertId <String>]`: Получает или задает идентификатор оповещения.
  - `[AlertProperty <IAlertModelAlertProperties>]`: Свойства оповещения.
    - `[(Any) <String>]`: Это указывает на то, что в этот объект можно добавить любое свойство.
  - `[ClosedByUserAlias <String>]`: Псевдоним пользователя, который закрыл оповещение.
  - `[ClosedTimestamp <String>]`: Метка времени закрытия оповещения.
  - `[CreatedTimestamp <String>]`: Метка времени создания оповещения.
  - `[Description <IDictionary[]>]`: Описание оповещения.
  - `[FaultId <String>]`: Получает или задает идентификатор ошибки оповещения.
  - `[FaultTypeId <String>]`: Получает или задает идентификатор типа ошибки для оповещения.
  - `[HasValidRemediationAction <Boolean?>]`: Указывает, можно ли исправить предупреждение.
  - `[ImpactedResourceDisplayName <String>]`: Отображаемое имя затронутого элемента.
  - `[ImpactedResourceId <String>]`: Возвращает или задает идентификатор ресурса для затронутого элемента.
  - `[LastUpdatedTimestamp <String>]`: Метка времени последнего обновления оповещения.
  - `[Remediation <IDictionary[]>]`: Получает или задает понятные инструкции по исправлению для оповещения.
  - `[ResourceProviderRegistrationId <String>]`: Получает или задает идентификатор регистрации службы, которой принадлежит оповещение.
  - `[ResourceRegistrationId <String>]`: Возвращает или задает идентификатор регистрации ресурса, связанного с оповещением. Если оповещение не связано с ресурсом, идентификатор регистрации ресурса равен null.
  - `[Severity <String>]`: Серьезность оповещения.
  - `[State <String>]`: Состояние оповещения.
  - `[Title <String>]`: Возвращает или задает идентификатор ресурса для затронутого элемента.

INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : параметр Identity
  - `[AlertName <String>]`: Имя оповещения.
  - `[Id <String>]`: Путь к удостоверению ресурса
  - `[Location <String>]`: Имя области
  - `[ResourceGroupName <String>]`: Имя группы ресурсов.
  - `[ResourceRegistrationId <String>]`: Идентификатор регистрации ресурса.
  - `[ServiceHealth <String>]`: Имя работоспособности службы.
  - `[ServiceRegistrationId <String>]`: Регистрационный идентификатор службы.
  - `[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ

