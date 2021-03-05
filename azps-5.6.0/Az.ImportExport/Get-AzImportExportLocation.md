---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: 928ac0254619a2924421a0b52bf20212b8ba19a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962984"
---
# Get-AzImportExportLocation

## SYNOPSIS
Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.
Расположение — это регион Azure.

## СИНТАКСИС

### Список (по умолчанию)
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Получить
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## ОПИСАНИЕ
Возвращает сведения о расположении, в которое можно отгрузить диски, связанные с заданием импорта или экспорта.
Расположение — это регион Azure.

## ПРИМЕРЫ

### Пример 1. Получите все сведения о расположении региона Azure с контекстом по умолчанию
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

Этот cmdlet получает все сведения о расположении региона Azure с контекстом по умолчанию.

### Пример 2. Просмотр сведений о расположении региона Azure по имени расположения
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

Этот cmdlet получает сведения о расположении региона Azure по имени расположения.

### Пример 3. Просмотр сведений о расположении региона Azure по удостоверениям
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

С помощью этих списков можно отсюдить сведения о расположении региона Azure по удостоверениям.

## PARAMETERS

### -AcceptLanguage
Указывает предпочтительный язык для ответа.

```yaml
Type: System.String
Parameter Sets: (All)
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

### -InputObject
Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Имя расположения.
Например, "Запад США" или "запад".

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity

## OUTPUTS

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation

## ПРИМЕЧАНИЯ

ALIASES

СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ

Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства. Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.


INPUTOBJECT <IImportExportIdentity> : Параметр identity
  - `[Id <String>]`: путь удостоверения ресурса
  - `[JobName <String>]`: имя задания импорта и экспорта.
  - `[LocationName <String>]`: название расположения. Например, "Запад США" или "запад".
  - `[ResourceGroupName <String>]`. Имя группы ресурсов однозначно определяет группу ресурсов в рамках подписки пользователя.
  - `[SubscriptionId <String>]`: ИД подписки для пользователя Azure.

## СВЯЗАННЫЕ ССЫЛКИ

