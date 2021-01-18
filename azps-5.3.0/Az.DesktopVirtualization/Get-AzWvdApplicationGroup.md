---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdApplicationGroup.md
ms.openlocfilehash: 5f2ccffd0b0ba82b215db018ee15f4e495704f15
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516874"
---
# Get-AzWvdApplicationGroup

## SYNOPSIS
Получите группу приложений.

## СИНТАКСИС

### Список1 (по умолчанию)
```
Get-AzWvdApplicationGroup [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Получить
```
Get-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Список
```
Get-AzWvdApplicationGroup -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## ОПИСАНИЕ
Получите группу приложений.

## ПРИМЕРЫ

### Пример 1. Получение группы приложений Virtual Desktop для Windows по имени
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

Эта команда получает группу приложений Виртуального рабочего стола Windows в группе ресурсов.

### Пример 2. Список групп приложений виртуального рабочего стола Windows
```powershell
PS C:\> Get-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName

Location   Name                  Type
--------   ----                  ----
eastus     ApplicationGroupName1 Microsoft.DesktopVirtualization/applicationgroups
eastus     ApplicationGroupName2 Microsoft.DesktopVirtualization/applicationgroups
```

Эта команда содержит список групп приложений Виртуального рабочего стола Windows в группе ресурсов.

## PARAMETERS

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

### -Filter
Выражение фильтра OData.
Допустимые свойства фильтрации — applicationGroupType.

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя группы приложений

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Имя группы ресурсов.
Имя нечувствительно к делу.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ИД целевой подписки.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplicationGroup

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity
  - `[ApplicationGroupName <String>]`: имя группы приложений
  - `[ApplicationName <String>]`: имя приложения в указанной группе приложений
  - `[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола
  - `[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов
  - `[Id <String>]`: путь удостоверения ресурса
  - `[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool
  - `[ResourceGroupName <String>]`: Имя группы ресурсов. Имя нечувствительно к делу.
  - `[SessionHostName <String>]`: имя сеанса в указанном пуле хостов
  - `[SubscriptionId <String>]`: ИД целевой подписки.
  - `[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса
  - `[WorkspaceName <String>]`: имя рабочей области

## СВЯЗАННЫЕ ССЫЛКИ

